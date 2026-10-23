# Compatibility

| Surface | Support |
| --- | --- |
| Modern evergreen browsers | Supported |
| ES modules | Required for `cybercore.js` and `contact.js` |
| CSS custom properties | Required |
| `prefers-reduced-motion` | Supported |
| Plain HTML | Supported |
| Vite / Astro / React | Supported through package or copied `dist/` |
| Server-side rendering | CSS is safe; load runtime on the client |
| Legacy browsers without modules | Not supported |

The `dist/v1/webkit.json` file is the capability contract for the current major Web Kit line. New major versions may change runtime APIs or generated asset paths.
