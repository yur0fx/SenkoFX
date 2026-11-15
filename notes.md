## Senko FX 1.10.1: faster, no extra settings

Every effect is just faster now. No Best/Fast switch: the 1.10.0 "Preview Speed" Draft option is gone (hidden, so projects saved with 1.10.0 still open).

- All whole-frame passes now run on every CPU core (48 passes ran on one core before), one shared worker pool that fits After Effects multi-frame rendering, faster pixel sampling, blurs, glows, noise and mirror edges.
- Smarter motion-blur sampling in Seamless, Radial Burst, Lens Tunnel, Swirl Lines and Shake (fewer samples where the picture barely moves). Prism Shards remembers its shard layout per area instead of rebuilding it per pixel.
- Same look: every preset of every effect was rendered at 1920x1080 with 1.9.0 and 1.10.1 and compared pixel by pixel. Most are identical; the rest differ by less than 1/255 on all but a handful of pixels (PSNR 62 dB or better).

Per frame, 1920x1080, average over all presets, 4-core CPU (offline bench of the effect code; in After Effects the shared thread pool should help more when several frames render at once):

| Effect | 1.9.0 | 1.10.1 | Faster |
|---|---:|---:|---:|
| Senko Seamless | 1475 ms | 969 ms | 1.5x |
| Senko Radial Burst | 559 ms | 330 ms | 1.7x |
| Senko Lens Tunnel | 554 ms | 298 ms | 1.9x |
| Senko Mosh | 510 ms | 426 ms | 1.2x |
| Senko Prism Shards | 422 ms | 245 ms | 1.7x |
| Senko Liquid Chrome | 365 ms | 286 ms | 1.3x |
| Senko Swirl Lines | 349 ms | 208 ms | 1.7x |
| Senko Speed Burst | 341 ms | 239 ms | 1.4x |
| Senko Dream Focus | 328 ms | 228 ms | 1.4x |
| Senko Prism Flow | 285 ms | 195 ms | 1.5x |
| Senko Rainbow Lines | 280 ms | 260 ms | 1.1x |
| Senko Kaleido | 271 ms | 215 ms | 1.3x |
| Senko Smear | ~ same | ~ same | 1.0-1.1x |
| Senko Spectrum Echo | 223 ms | 156 ms | 1.4x |
| Senko Rainbow Wave | 208 ms | 174 ms | 1.2x |
| Senko Neon Grade | 173 ms | 142 ms | 1.2x |
| Senko CRT Finish | 159 ms | 117 ms | 1.4x |
| Senko Pixel Dust | 158 ms | 140 ms | 1.1x |
| Senko One Framer | 152 ms | 123 ms | 1.2x |
| Senko Toon Flatten | ~ same | ~ same | 1.0-1.1x |
| Senko Shake | 139 ms | 78 ms | 1.8x |
| Senko Glitch Window | 123 ms | 91 ms | 1.3x |
| Senko Tile Shift | 114 ms | 94 ms | 1.2x |
| Senko Chrome Relief | 109 ms | 87 ms | 1.3x |
| Senko Light Leak | ~ same | ~ same | 1.0-1.1x |
| Senko Target HUD | 72 ms | 50 ms | 1.4x |
| Senko Frame Box | 68 ms | 62 ms | 1.1x |
| Senko Glow Key | 62 ms | 58 ms | 1.1x |
| Senko Mosaic Patches | 26 ms | 24 ms | 1.1x |
| Senko Block Glitch | 23 ms | 20 ms | 1.2x |
| Senko Cut Kit | 13 ms | 12 ms | 1.1x |

Install: close After Effects, unzip **SenkoFX-Setup-1.10.1.zip**, run the Setup. Senko FX 1.7.1 and later update themselves.
