# Svelte + Vite + PWA

## How to


1. Create the following files and update accoring to your repo
  - service-worker.js
  - manifest.webmanifest
  - icons
  - maskable icon
  - CNAME file for GitHub Pages

2. Install gh-pages

```bash
pnpm i -D gh-pages
```

3. Update package.json scripts

```json
 "scripts": {
    "dev": "vite",
    "build": "vite build && cp service-worker.js CNAME ./dist ",
    "preview": "vite preview",
    "deploy": "npx gh-pages -d dist"
  },
```

4. Run command

```bash
npm run build && npm run deploy
```

5. Check the site with Lighthouse

![PWA](./images/pwa.png)