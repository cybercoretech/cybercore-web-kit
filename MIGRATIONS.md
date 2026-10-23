# 🚢 Migration notes

## ✨ 1.0.0

- First standalone Web Kit release.
- Versioned browser assets live under `dist/v1/`.
- Theme registry and contact data are included under `dist/data/`.
- `window.SITE.dataRoot` can point to the bundled snapshot or the shared Cybercore registry.
- The runtime exposes `window.CybercoreWebKit` with `version` and `applyRecipes`.

When upgrading a minor release, keep the `v1` asset paths and review `dist/build.json` for the source revision and registry snapshot. A major release will receive a new version directory and migration entry.
