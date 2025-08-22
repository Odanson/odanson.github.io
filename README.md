# odanson.github.io — Samson Odan

Personal research website built with plain HTML + Tailwind.

## Quick start
- Open `index.html` locally in a browser (no build step).
- Dark mode toggle persists via `localStorage`.
- Sidebar is sticky on desktop, off‑canvas on mobile.

## Structure
- `index.html` — all content + JS for rendering sections.
- `Samson_Odan_CV.pdf` — downloadable CV.
- `portrait.jpg` — avatar (~400×400 recommended).
- Favicons: `favicon.ico`, `favicon-192.png`, `favicon-512.png`, `apple-touch-icon.png`.
- Optional `pubs.json` — extra publications merged into the page at runtime.

## Publications
- Two “built‑in” items are defined in `index.html` under `let PUBS = [...]`.
- At load, the site merges:
  1. Built‑ins,
  2. `pubs.json` (if present),
  3. Any items stored in `localStorage` (from the admin importer).
- Use `?admin` locally to show the BibTeX import box (hidden on production):
  - Drag‑drop a `.bib` file to import.
  - **Export** merges via the “Export pubs.json” button.
  - **Clear local** resets `localStorage` to defaults + file pubs.

## Favicons
Generated with ImageMagick from a square PNG. Links are wired in `<head>`.

## Social/SEO
Open Graph + Twitter Card meta, canonical URL, person JSON‑LD, and per‑item pubs JSON‑LD.

## Deploy
Push to `main`; GitHub Pages serves from the repo.
Hard‑refresh to bust caches (Cmd/Ctrl+Shift+R).
