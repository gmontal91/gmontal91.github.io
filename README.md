# GMA landing

Static landing page built with [Vite](https://vite.dev/), styled for GitHub Pages (`base: './'` so asset paths stay correct when hosted under a project URL).

## Develop

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## GitHub Pages

1. Repo **Settings → Pages**: set **Source** to **GitHub Actions** (recommended).
2. Push to `main` or `master`; the workflow in `.github/workflows/deploy-pages.yml` builds and deploys `dist/`.

If your site is `https://<user>.github.io/<repo>/` and anything breaks, set `base` in `vite.config.js` to `'/<repo>/'` instead of `'./'`.

Replace copy in `src/main.js`, swap `public/portrait.svg` for a photo, update social `href`s, and connect the newsletter form to your provider (Buttondown, Mailchimp, etc.).
