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

1. Repo **Settings → Pages** → **Build and deployment** → **Source**: seleziona **GitHub Actions** (non *Deploy from a branch* sulla root del repo).
2. Fai push su `main` o `master`, oppure avvia manualmente il workflow **Actions → Deploy to GitHub Pages → Run workflow**. Il workflow esegue `npm run build` e carica solo il contenuto di **`dist/`**.

### Se vedi errori MIME su `/src/style.css` o `/src/assets/...`

Significa che Pages sta servendo i **sorgenti** Vite (cartella del repo) invece della **build**. In quel caso il browser prova a importare file raw come moduli ES e blocca CSS/SVG. **Soluzione:** imposta la sorgente Pages su **GitHub Actions** e attendi un deploy riuscito (oppure pubblica manualmente il contenuto di `dist/` nella branch/target corretti).

Sito in sottocartella `https://<user>.github.io/<repo>/`: in `vite.config.js` imposta `base: '/<repo>/'` (sostituisci `<repo>` con il nome del repository).

Replace copy in `src/main.js`, swap `public/portrait.svg` for a photo, update social `href`s, and connect the newsletter form to your provider (Buttondown, Mailchimp, etc.).
