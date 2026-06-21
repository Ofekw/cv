# CV

A one-page CV maintained as a single Markdown file ([`cv.md`](./cv.md)) that builds
into a self-contained single-page website and exports cleanly to PDF.

## How it works

- **`cv.md`** is the single source of truth: YAML front-matter (name, title, tagline,
  contact, links) plus a Markdown body for the sections.
- **`build.mjs`** renders it into **`dist/index.html`** — one self-contained file with
  the CSS inlined, so it works anywhere and prints identically. It also renders the
  **Thoughts** blog from [`posts/`](./posts) (see below).
- The design lives in **`src/styles.css`** and the page shells in **`src/template.html`**
  (CV), **`src/post.html`** (a post) and **`src/thoughts.html`** (the post list).

## Edit & build

```bash
npm install      # first time only
npm run build    # writes dist/index.html
```

Then open `dist/index.html` in a browser. To iterate, edit `cv.md` (or the styles) and
re-run `npm run build`.

## Thoughts (blog)

Posts live in [`posts/`](./posts) as Markdown with YAML front-matter:

```markdown
---
title: "Your post title"
date: 2026-06-20
draft: false
summary: "One or two sentences shown in the list and as the page description."
tags:
  - distributed-systems
  - caching
---

Body in Markdown. Skip the leading H1 — the title comes from front-matter.
```

- The build emits a list page at **`dist/thoughts/index.html`** and one page per post at
  **`dist/thoughts/<filename>/index.html`** (the filename is the slug, so `posts/1m-rps.md`
  publishes to `/thoughts/1m-rps/`). Posts are listed newest-first by `date`.
- Set **`draft: true`** to keep a post out of the build entirely; flip it to `false` to publish.
- Fenced ` ```mermaid ` code blocks render as diagrams client-side via the Mermaid CDN. No
  build step is needed for them; just write the diagram in the post.
- The site nav (CV / Thoughts) is added automatically and is hidden when printing, so the CV
  still exports as a clean single page.

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
