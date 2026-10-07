# nuvio-art

Artwork for my Nuvio collections, served free through the jsDelivr CDN.

| Folder | Content | Size |
| --- | --- | --- |
| `livesports/covers/` | Live Sports poster covers | 1000×1414 (2:3) |
| `livesports/gifs/` | Live Sports animated focus GIFs | 540×764 (2:3) |
| `fixes/` | 16:9 replacements for square covers (Lucasfilm, MGM+) | 1000×563 |

URL pattern:

```
https://cdn.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>
```

The repo must stay **public**: raw/jsDelivr URLs of a private repo return 404.

To change an image, overwrite the file with the same name and push. jsDelivr refreshes `@main`
within ~12 h, or right away by opening `https://purge.jsdelivr.net/gh/MatizS27/nuvio-art@main/<path>`.
