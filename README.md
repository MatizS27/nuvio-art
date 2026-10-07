# nuvio-art

Artwork for my Nuvio collections, served straight from GitHub (raw.githubusercontent.com).

| Folder | Content | Size |
| --- | --- | --- |
| `livesports/covers/` | Live Sports poster covers | 1000×1414 (2:3) |
| `livesports/gifs/v3/` | Live Sports focus GIFs: ~0.2 s grey→colour transition (20 ms per frame, no pause at the start) plays once, then holds on the last frame | 540×764 (2:3) |
| `livesports/gifs/v2/` | Previous Live Sports focus GIFs (~0.47 s transition), kept so old URLs still work | 540×764 (2:3) |
| `livetv/covers/` + `livetv/gifs/v1/` | Live TV cover and focus GIF in the Live Sports style (wall of sports screens, white TV icon, red LIVE dot in colour) | 1000×1414 cover / 540×764 GIF |
| `hover/v1/<collection>/` | Hover GIFs for Kaptain folders: 0.2 s crossfade cover → hover art, plays once, holds (Spotlight also has a pinned `-cover.jpg`) | 341×512 poster / 512×288 landscape |
| `fixes/` | 16:9 replacements for square covers (Lucasfilm, MGM+) | 1000×563 |

URL pattern:

```
https://raw.githubusercontent.com/MatizS27/nuvio-art/main/<path>
```

The repo must stay **public**: raw URLs of a private repo return 404.

Don't use jsDelivr (`cdn.jsdelivr.net/gh/...`): the repo is over its 50 MB package limit, so it sometimes
answers with a "Package size exceeded" text instead of the image, and Nuvio caches that text as a broken GIF.

To change an image, overwrite the file with the same name and push; raw URLs refresh within ~5 minutes.

Nuvio desktop only shows a focus image when it has **more than one frame** (single-frame GIF/JPEG/PNG "hovers" are ignored) and scales it to max 512 px.
Focus GIFs have no loop extension (play once) and their last frame lasts 65535 cs (~10.9 min), because
Nuvio desktop ignores the GIF loop count and always loops. When replacing one, publish it under a new path
(e.g. `gifs/v3/`) so Nuvio's own GIF disk cache doesn't keep serving the old file.
