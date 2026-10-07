# nuvio-art

Artwork for my Nuvio collections, served free through the jsDelivr CDN.

| Folder | Content | Size |
| --- | --- | --- |
| `livesports/covers/` | Live Sports poster covers | 1000×1414 (2:3) |
| `livesports/gifs/v3/` | Live Sports focus GIFs: ~0.2 s grey→colour transition (20 ms per frame, no pause at the start) plays once, then holds on the last frame | 540×764 (2:3) |
| `livesports/gifs/v2/` | Previous Live Sports focus GIFs (~0.47 s transition), kept so old URLs still work | 540×764 (2:3) |
| `hover/v1/<collection>/` | Hover GIFs for Kaptain folders: 0.2 s crossfade cover → hover art, plays once, holds (Spotlight also has a pinned `-cover.jpg`) | 341×512 poster / 512×288 landscape |
| `fixes/` | 16:9 replacements for square covers (Lucasfilm, MGM+) | 1000×563 |

URL pattern:

```
https://cdn.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>
```

The repo must stay **public**: raw/jsDelivr URLs of a private repo return 404.

To change an image, overwrite the file with the same name and push. jsDelivr refreshes `@main`
within ~12 h, or right away by opening `https://purge.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>`.

Nuvio desktop only shows a focus image when it has **more than one frame** (single-frame GIF/JPEG/PNG "hovers" are ignored) and scales it to max 512 px.
Focus GIFs have no loop extension (play once) and their last frame lasts 65535 cs (~10.9 min), because
Nuvio desktop ignores the GIF loop count and always loops. When replacing one, publish it under a new path
(e.g. `gifs/v3/`) so Nuvio's own GIF disk cache doesn't keep serving the old file.
