# World Cup 2026 — Knockout Bracket

Interactive radial bracket for the FIFA World Cup 2026 knockout stage. Tap a flag to advance a team, reset picks, or share your bracket via the URL hash.

The app itself lives in [`table.html`](table.html). This repo adds a thin static wrapper so you can run it locally and deploy it to GitHub Pages or Vercel without changing the HTML.

## Local development

```bash
npm install
npm run dev
```

Open [http://localhost:3000/table.html](http://localhost:3000/table.html).

To preview the production build:

```bash
npm run build
npm run preview
```

## Deploy

### GitHub Pages

1. In the repo on GitHub, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Push to `main`. The workflow in [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) builds and publishes the site.

Your site will be available at `https://<username>.github.io/knockout-table/`.

### Vercel

1. Import this repo in [Vercel](https://vercel.com).
2. Vercel picks up [`vercel.json`](vercel.json) automatically (`npm run build` → `dist/`).
3. Deploy.

No environment variables or server configuration required.

## Project layout

```
table.html          # the app (unchanged)
index.html          # local dev redirect to table.html
scripts/build.mjs   # copies table.html → dist/index.html for deploy
dist/               # build output (gitignored)
```
