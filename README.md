# GMA landing

Sito statico: `index.html`, `styles.css`, cartella `assets/` (logo, ritratto). Nessun bundler: adatto a **GitHub Pages** anche con *Deploy from branch* sulla root del repo.

## Modificare i contenuti

- Testo e sezioni: `index.html`
- Stili: `styles.css`
- Logo: `assets/logo.svg` · Ritratto: `assets/portrait.svg` · Favicon: `favicon.svg`

## Anteprima locale

Apri `index.html` nel browser oppure, dalla cartella del progetto:

```bash
python3 -m http.server 8080
```

Poi visita `http://localhost:8080`.

## GitHub Pages

**Opzione A — dalla branch (senza Actions)**  
Settings → Pages → Source: branch `main`, cartella `/ (root)`. Assicurati che in root ci siano `index.html`, `styles.css`, `favicon.svg`, `.nojekyll` e `assets/`.

**Opzione B — GitHub Actions**  
Source: **GitHub Actions**. Il workflow copia i file statici in `_site/` e li pubblica (vedi `.github/workflows/deploy-pages.yml`).

Sito in sottocartella `https://<user>.github.io/<repo>/`: in `index.html` aggiorna i percorsi (es. `./styles.css` → `./<repo>/styles.css`) oppure usa un `<base href="...">` coerente.

---

Modulo newsletter: messaggio di conferma gestito da uno script inline in `index.html`; collegalo al tuo provider quando sei pronto.
