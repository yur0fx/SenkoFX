## Senko FX 1.11.0: compositing effects

8 new effects for putting cut-outs, keyed clips and stock elements into a shot. 39 effects in total. Most have a **Background Layer** picker: choose the layer behind, and the effect takes its light, colour and grain from it. Same size as your layer (both comp size) lines up pixel for pixel; a different size is stretched to fit. No layer picked still works (colour controls instead).

- **Senko Light Wrap**: background light spills over the layer's edges so it sits in the shot. Screen / Add / Normal / Soft Light / Wrap Only, bright parts only, reach inside. 7 presets.
- **Senko Edge Blend**: choke or grow and feather the matte, swap dirty edge colour for the colour just inside, kill dark / light halos and green / blue spill, lean the edge toward the background. Views for edge zone and matte. 7 presets.
- **Senko Colour Match**: matches the layer's colour, brightness, contrast and black / white points to the background layer (or to a target colour), looking at the whole background or just near the layer, with skin / white protection. 6 presets.
- **Senko Shadow**: drop shadow, contact shadow and a cast shadow laid on the ground that gets softer and fainter with height. Shadow colour can take the background's hue. Shadow Only output. 7 presets.
- **Senko Rim Light**: anime rim light along the edge from a light direction, coloured by a colour or by the background behind it, with wrap-around, outer glow and hard cel edge. 7 presets.
- **Senko Depth Fog**: fog and haze that thickens with distance (screen height, brightness, distance from a point, or a depth layer), drifting mist, haze blur, colour from the sky. 7 presets.
- **Senko Key Clean**: fast green / blue / any-colour screen key with clip black / white, choke, soft edge and spill kill that puts back neutral light or the new background's light. 6 presets.
- **Senko Grain Match**: film / anime grain; with Match Background Grain it measures the noise in the background layer and adds just enough to match. Grain size, colour grain, shadows / midtones / highlights, on 2s / 3s / still. 6 presets.

Fast by default, no quality setting: 20-130 ms per 1920x1080 frame on a 4-core CPU (offline bench of the effect code), big blurs run at reduced size, everything on every core.

The other 31 effects are unchanged (rebuilt with the new shared code). Untested in real After Effects yet.

![New in 1.11.0](https://raw.githubusercontent.com/yur0fx/SenkoFX/main/images/new-in-1.11.0.png)
