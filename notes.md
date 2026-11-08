## Senko FX 1.7.1: automatic updates

Senko FX now keeps itself up to date. Install this version once, and from then on new versions install in the background while After Effects is closed.

- A Windows scheduled task ("Senko FX Updater") checks this repo's latest release at logon and every 3 hours.
- It only downloads from the yur0fx/SenkoFX releases and checks the SHA-256 before installing.
- To turn it off, set the DWORD `AutoUpdate` to `0` under `HKLM\Software\Senko FX`, or disable the task in Task Scheduler. Uninstalling Senko FX removes it.

Everything from 1.7.0 is included: eight new effects (Block Glitch, Chrome Relief, Toon Flatten, Glow Key, Target HUD, Mosaic Patches, Swirl Lines, CRT Finish) and the Mosh Whole Clip datamosh mode. 29 effects in total.

![New in 1.7.0](https://raw.githubusercontent.com/yur0fx/SenkoFX/main/images/new-in-1.7.0.png)

### Install
1. Close After Effects.
2. Unzip **SenkoFX-Setup-1.7.1.zip** and run `SenkoFX-Setup-1.7.1.exe` (it asks for admin). It installs over older versions.
3. Open After Effects and look under **Effect > Senko FX**.

Manual install: copy the .aex files from `SenkoFX-plugins-1.7.1.zip` to `C:\Program Files\Adobe\Common\Plug-ins\7.0\MediaCore\Senko FX` (no auto update that way).

Windows x64, CPU only (runs on any GPU or none), 8/16/32 bpc.

SHA-256:
```
bf0083470a77d25b48a30f4460165ba0fda9603b1a20bca029c6e505f166772f  SenkoFX-Setup-1.7.1.zip
0563e5b721d784aac2f2c0c225ed1be4f18c43f95b8698bf34771630701fc341  SenkoFX-plugins-1.7.1.zip
```
