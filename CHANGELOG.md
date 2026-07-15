# Changelog

All notable changes to the CartonCrewStudio site are documented here.
This project follows [Semantic Versioning](https://semver.org/).

## [1.0.1] — 2026-07-15

### Added
- Gitleaks secret scanning on every pull request and every push to `main` (`AB#331`). Uses the
  upstream gitleaks binary rather than `gitleaks-action`, which requires a paid licence for org
  accounts. This repo previously had **no secret scanning at all** — and it is **public**, so a
  credential committed here would be world-readable the moment it landed.
- `.gitleaks.toml` extending the upstream default ruleset with the credential shapes ChAImp uses.

### Notes
- **Full-history scan at this version: clean.** 1 commit scanned, no findings.
- No allowlist entries beyond the standard `.env.example` path. Unlike `chaimp-website`, this repo
  carries no Cloudflare beacon token, so it needs no exemption for one — every allowlist entry is a
  hole, and holes are not added pre-emptively.
- GitHub Pages deployment is unaffected.

## [1.0.0] — 2026-06-29

### Added
- Initial CartonCrewStudio early-access / waitlist site (`index.html`).
- Hero with animated watercolor washes, brand lockup, and "speaks gallery" headline.
- Feature section for the five first-class record types: Artists, Works,
  Exhibitions, Patrons, Programs.
- AI relationship-memory section with an illustrative prompt card.
- "Built on CartonCrew / by ChAImp" trust section.
- Waitlist form wired to Formspree (AJAX + honeypot + no-JS fallback).
- Full SEO: meta description/keywords, canonical, Open Graph + Twitter cards,
  `Organization` + `WebSite` + `SoftwareApplication` JSON-LD, `sitemap.xml`,
  `robots.txt`, favicons, and a generated 1200×630 social share image.
- GitHub Pages hosting config: `CNAME` (cartoncrew.art) and `.nojekyll`.
- Accessibility: semantic landmarks, alt text, focus styles, and a
  `prefers-reduced-motion` guard on all animation.
