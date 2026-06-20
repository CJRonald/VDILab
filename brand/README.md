# VDI Lab — Brand Assets

VDI Lab (Visual-Driven Intelligence Lab) logo source files. Designed 2026-04-26.

**Palette**: navy `#0B2545` + teal `#00A39A` (Visual-Driven Intelligence).

## Files

| Family | Description | Variants |
|--------|-------------|----------|
| `vdi-monogram` | V–D–I letter monogram | color + `-mono` |
| `vdi-mark-hexnodes` | Hexagon-node mark (neural / vision motif; the lab's primary mark) | color + `-mono` |
| `vdi-lockup-flanking` | Horizontal lockup (mark + wordmark, for headers) | light + `-dark` |
| `vdi-favicon-bold` | Favicon-optimized hexnode (bolder strokes, dropped faint guide lines) | SVG only |

Each family has `.svg` (vector source, edit this) + `.png` (1024² mark / 1800×440 lockup).

## Deployed favicon

The site favicon is derived from `vdi-favicon-bold.svg` → rendered to
`favicon.svg` / `favicon.ico` (16/32/48) / `favicon-16.png` / `favicon-32.png` /
`apple-touch-icon.png` in the **VDILab repo root** (and copied to
`cjhuang-site/assets/img/`). To regenerate:

```bash
rsvg-convert -w 32  brand/vdi-favicon-bold.svg -o favicon-32.png
rsvg-convert -w 16  brand/vdi-favicon-bold.svg -o favicon-16.png
rsvg-convert -w 180 brand/vdi-favicon-bold.svg -o apple-touch-icon.png
# favicon.ico (multi-size) via Pillow: see Homepage PROGRESS 2026-06-20
```

These source files are the SSOT for the lab's visual identity — reuse for
slides, posters, business cards, etc.
