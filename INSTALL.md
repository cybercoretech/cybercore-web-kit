# 🚀 Installation

The Web Kit is dependency-free. Choose the integration style that matches the host project.

## ✨ Plain HTML

```html
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/tokens.css">
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/components.css">
<link rel="stylesheet" href="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/effects.css">
<script>
  window.SITE = {
    dataRoot: 'https://cybercoretech.github.io/cybercore-web-kit/dist/data',
    defaultTheme: 'cybercore-tech',
    web: { motion: 'full' }
  };
</script>
<script type="module" src="https://cybercoretech.github.io/cybercore-web-kit/dist/v1/cybercore.js"></script>
```

Add a chooser anywhere in the page:

```html
<div class="theme-picker">
  <button id="themeButton" aria-expanded="false">SELECT THEME</button>
  <div id="themeMenu" role="listbox" hidden></div>
</div>
```

## ✨ Vite, Astro, or React

Install the optional package from a release or copy the `dist/` directory into the project:

```bash
npm install @cybercore/web-kit
```

```js
import '@cybercore/web-kit/v1/tokens.css';
import '@cybercore/web-kit/v1/components.css';
import '@cybercore/web-kit/v1/effects.css';
import '@cybercore/web-kit/v1/cybercore.js';
```

For Astro and React, load the CSS from the application entrypoint and render the chooser markup in a client-rendered component. The engine is browser-only and should not be evaluated during server rendering.

## ✨ Other projects

For any static host, download a tagged archive, copy `dist/`, and point `window.SITE.dataRoot` at the included `dist/data/` snapshot. Use the remote registry only when live catalog updates are preferred over offline reproducibility.

## ✨ Accessibility and motion

The runtime respects `prefers-reduced-motion`. Set `window.SITE.web.motion` to `full`, `reduced`, or `none` to select a stricter project policy.
