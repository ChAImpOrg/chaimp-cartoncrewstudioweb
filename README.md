# CartonCrewStudio — marketing site

The early-access / waitlist site for **CartonCrewStudio**, the nonprofit CRM
built for art galleries and community studios. A CartonCrew spin-off by
[ChAImp](https://chaimp.org).

- **Live domain:** https://cartoncrew.art
- **Hosting:** GitHub Pages (custom domain via `CNAME`)
- **Stack:** single static `index.html` (no build step), embedded CSS + vanilla JS

## Structure

| File | Purpose |
|------|---------|
| `index.html` | The whole site — hero, features, AI-memory, trust, waitlist, footer |
| `CartonCrewStudio_Logo.png` | Brand lockup (whitespace-trimmed) |
| `favicon.png`, `apple-touch-icon.png` | Icons (derived from the logo box) |
| `og-image.png` | 1200×630 social share image |
| `CNAME` | `cartoncrew.art` for GitHub Pages |
| `robots.txt`, `sitemap.xml` | SEO crawl directives |
| `.nojekyll` | Serve files as-is (skip Jekyll) |

## Waitlist form

The waitlist posts to **Formspree** (`/f/xpqgjzap`) via AJAX, with a normal
POST fallback if JavaScript is off. A hidden `_gotcha` honeypot guards spam.
To change the destination, update the `<form action>` in `index.html`.

## Local preview

```sh
python -m http.server 8000
# open http://localhost:8000
```

## Brand tokens

Navy `#0B2E66` · Teal `#00B488` · Yellow `#F4B71E`, plus watercolor accents —
sampled from the logo, kept consistent with the ChAImp / CartonCrew family.

<!-- AB#318 anti-deadlock probe - closed unmerged, never lands -->
