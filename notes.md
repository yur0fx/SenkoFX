## Senko FX 1.10.0: faster previews

All 31 effects render faster, and a new Draft path makes previews near-instant. Final renders look the same as 1.9.0.

- **Faster at Best quality**: one shared pool of worker threads instead of new threads for every pass (After Effects renders several frames at once, so 1.9.0 could start dozens of threads per frame), faster pixel sampling, blurs and mirror edges, and smarter motion-blur sampling in Seamless, Radial Burst, Lens Tunnel, Swirl Lines and Shake (fewer samples where the picture barely moves). Seamless, Lens Tunnel and Radial Burst are about 1.5-1.9x faster.
- **Draft quality = fast preview**: set the layer's Quality switch to Draft (or use Fast Draft) and the effect renders at half size and scales up, about 3-6x faster. New control in every effect: **Preview Speed > Draft Quality Renders At** (Half Size / Quarter Size / Full Size). Best quality and the Render Queue (Best by default) are never affected.
- Same look: every preset of every effect was rendered at 1920x1080 with 1.9.0 and 1.10.0 and compared pixel by pixel. Most are identical; the rest differ by less than 1/255 on all but a handful of pixels (PSNR 62 dB or better).

Per frame, 1920x1080, average over all presets, 4-core CPU (offline bench of the effect code):

| Effect | 1.9.0 Best | 1.10.0 Best | 1.10.0 Draft |
|---|---:|---:|---:|
| Senko Seamless | 1466 ms | 846 ms | 237 ms |
| Senko Lens Tunnel | 615 ms | 319 ms | 87 ms |
| Senko Radial Burst | 572 ms | 391 ms | 82 ms |
| Senko Mosh | 504 ms | 464 ms | 269 ms |
| Senko Prism Shards | 414 ms | 375 ms | 105 ms |
| Senko Swirl Lines | 384 ms | 281 ms | 79 ms |
| Senko Liquid Chrome | 347 ms | 327 ms | 97 ms |
| Senko Dream Focus | 345 ms | 248 ms | 61 ms |
| Senko Speed Burst | 325 ms | 253 ms | 74 ms |
| Senko Prism Flow | 282 ms | 236 ms | 70 ms |
| Senko Rainbow Lines | 271 ms | 272 ms | 75 ms |
| Senko Kaleido | 260 ms | 237 ms | 75 ms |
| Senko Rainbow Wave | 235 ms | 210 ms | 57 ms |
| Senko Smear | 220 ms | 203 ms | 153 ms |
| Senko Spectrum Echo | 215 ms | 185 ms | 46 ms |
| Senko Neon Grade | 177 ms | 181 ms | 63 ms |
| Senko Toon Flatten | 170 ms | 178 ms | 69 ms |
| Senko CRT Finish | 165 ms | 157 ms | 50 ms |
| Senko Pixel Dust | 154 ms | 152 ms | 57 ms |
| Senko One Framer | 149 ms | 128 ms | 38 ms |
| Senko Glitch Window | 144 ms | 122 ms | 39 ms |
| Senko Tile Shift | 126 ms | 111 ms | 42 ms |
| Senko Shake | 121 ms | 80 ms | 33 ms |
| Senko Chrome Relief | 112 ms | 100 ms | 39 ms |
| Senko Light Leak | 96 ms | 110 ms | 40 ms |
| Senko Frame Box | 88 ms | 83 ms | 27 ms |
| Senko Target HUD | 75 ms | 70 ms | 39 ms |
| Senko Glow Key | 68 ms | 59 ms | 29 ms |
| Senko Mosaic Patches | 28 ms | 32 ms | 23 ms |
| Senko Block Glitch | 27 ms | 27 ms | 25 ms |
| Senko Cut Kit | 8 ms | 9 ms | 15 ms |

Install: close After Effects, unzip **SenkoFX-Setup-1.10.0.zip**, run the Setup. Senko FX 1.7.1 and later update themselves.
