# nuvio-art

Artwork for my Nuvio collections, served free through the jsDelivr CDN.

| Folder | Content | Size |
| --- | --- | --- |
| `livesports/covers/` | Live Sports poster covers | 1000×1414 (2:3) |
| `livesports/gifs/v2/` | Live Sports focus GIFs: grey→colour transition plays once, then holds on the last frame | 540×764 (2:3) |
| `fixes/` | 16:9 replacements for square covers (Lucasfilm, MGM+) | 1000×563 |

URL pattern:

```
https://cdn.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>
```

The repo must stay **public**: raw/jsDelivr URLs of a private repo return 404.

To change an image, overwrite the file with the same name and push. jsDelivr refreshes `@main`
within ~12 h, or right away by opening `https://purge.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>`.

Focus GIFs have no loop extension (play once) and their last frame lasts 65535 cs (~10.9 min), because
Nuvio desktop ignores the GIF loop count and always loops. When replacing one, publish it under a new path
(e.g. `gifs/v3/`) so Nuvio's own GIF disk cache doesn't keep serving the old file.
