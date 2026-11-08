# ✨ Cybercore Web Kit

The standalone, dependency-free browser distribution for Cybercore themes, tokens, components, effects, and shared contact surfaces.

## ✨ Use from HTML

```html
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/tokens.css">
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/components.css">
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/effects.css">
<script type="module" src="https://cybercoretech.github.io/cybercore-web-kit/dist/contact.js"></script>
<script type="module" src="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/cybercore.js"></script>
```

The kit has no runtime dependency or bundler requirement. It works in plain HTML and can also be copied into Vite, Astro, React, and other frontend projects.

## ✨ Distribution layout

| Path | Purpose |
| --- | --- |
| `dist/v1/cybercore.js` | Theme engine, registry loading, palette application, and theme events |
| `dist/v1/tokens.css` | Shared design-token variables |
| `dist/v1/components.css` | Theme-aware component primitives |
| `dist/v1/effects.css` | Governed motion effects and reduced-motion fallbacks |
| `dist/contact.js` | Universal Cybercore contact element |
| `dist/chooser.js`, `dist/chooser.css` | Universal theme chooser, `<cybercore-theme-chooser>`: 600 registry themes + 12 signature mashups |
| `dist/v1/webkit.json` | Version, capabilities, source, and compatibility metadata |

## 🚢 Releases and source

This repository contains generated Web Kit artifacts. The canonical source and build process live in the [Cybercore Systems Framework](https://github.com/cybercoretech/cybercore), while the [Control Plane](https://github.com/cybercoretech/cybercore-control-plane) governs manifests, validation, and publishing plans.

`dist/` mirrors the live kit and theme data on [cybercoretech.github.io](https://cybercoretech.github.io/kit/), which is itself generated from cybercore. The *Sync from org kit* workflow (`.github/workflows/sync-org-kit.yml`) runs every 6 hours or on demand, mirrors the org site with cybercore's `tools/publish-web-kit.sh`, checks syntax and checksums, and opens a PR when anything changed. Do not edit `dist/` by hand; change cybercore instead (see its [docs/distribution.md](https://github.com/cybercoretech/cybercore/blob/main/docs/distribution.md)).

- [Live package directory](https://cybercoretech.github.io/cybercore-web-kit/dist/)
- [Theme registry](https://cybercoretech.github.io/data/)
- [Cybercore crates](https://crates.io/search?q=cybercore)
- [Control Plane documentation](https://cybercoretech.github.io/cybercore-control-plane/)

Every generated release should include its source revision, schema version, checksums, and compatibility metadata in `dist/v1/webkit.json`.

## ✨ Local preview

```bash
python3 -m http.server 8000
```

Open `http://127.0.0.1:8000/` and use the files under `dist/`.
