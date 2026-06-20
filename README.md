# CV

A one-page CV maintained as a single Markdown file ([`cv.md`](./cv.md)) that builds
into a self-contained single-page website and exports cleanly to PDF.

## How it works

- **`cv.md`** is the single source of truth: YAML front-matter (name, title, tagline,
  contact, links) plus a Markdown body for the sections.
- **`build.mjs`** renders it into **`dist/index.html`** — one self-contained file with
  the CSS inlined, so it works anywhere and prints identically.
- The design lives in **`src/styles.css`** and the page shell in **`src/template.html`**.

## Edit & build

```bash
npm install      # first time only
npm run build    # writes dist/index.html
```

Then open `dist/index.html` in a browser. To iterate, edit `cv.md` (or the styles) and
re-run `npm run build`.

## Export to PDF

Open `dist/index.html` and use the browser's **Print → Save as PDF** (Ctrl/Cmd-P). The
print stylesheet is tuned to produce a clean single page on US Letter, matching the site
exactly. Tips: set margins to **Default**, paper to **Letter**, and enable **Background
graphics** so the accent colour prints.

## Deploy (GitHub Pages)

Pushing to `master` triggers `.github/workflows/deploy.yml`, which builds and publishes
`dist/` to GitHub Pages. One-time setup: in the repo, go to **Settings → Pages → Build
and deployment → Source** and choose **GitHub Actions**. The site then publishes at
`https://ofekw.github.io/cv/`.

## Custom domain (ofek.io)

To serve this at `ofek.io`:

1. Create a file named `CNAME` in the repo root containing one line: `ofek.io`
   (the build copies it into `dist/` automatically).
2. At your DNS provider, point the apex domain at GitHub Pages with four `A` records:
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   (and optionally `AAAA` records for IPv6).
3. In **Settings → Pages → Custom domain**, enter `ofek.io` and enable **Enforce HTTPS**
   once the certificate is issued.
