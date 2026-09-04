# Embedded Financing Guide

**Read it online:**

- GitHub Pages — https://mark-denysenko.github.io/fintech-knowledge/
- Cloudflare Workers (mirror) — https://fintech-expert.mark-denyssenko.workers.dev/

Onboarding guide to multi-lender point-of-sale (POS) and embedded financing — the terms,
flows, diagrams, and A–Z glossary

Covers: the multi-lender waterfall, products (PLCC, DLOC, installment, BNPL, LTO, HELOC),
application & credit decisioning, offers & rate plans (with a decoded real plan object),
checkout & funding rails (VCC/VCN, card networks, Marqeta-style JIT funding), the postsale
transaction lifecycle, reconciliation, a compliance map with state-by-state variance, the
home-improvement vertical (staged funding, certificate of completion), and agentic commerce.

## Files

| Path | What it is |
|---|---|
| `index.html` | The complete guide as one self-contained page. **This is the file you open or host.** |
| `src/artifact-body.html` | The guide's source exactly as published in the Claude artifact (body-only fragment). The sync target for updates — see `UPDATING.md`. |
| `scripts/wrap_artifact.py` | Turns `src/artifact-body.html` into `index.html` (adds the document skeleton). No dependencies beyond Python 3. |
| `UPDATING.md` | How to pull the latest version from the Claude artifact into this repo. |

## Open locally

Just open `index.html` in a browser — no build step, no server needed.
Fonts load from Google Fonts when online; offline, the page falls back to system fonts and
stays fully readable. Light/dark theme follows your OS setting.

## Host as a static site

Serve the repo (or just `index.html`) from any static host — GitHub Pages, S3/CloudFront,
Netlify, nginx. There is nothing to build: one HTML file, zero runtime dependencies,
all CSS/JS inline, diagrams are inline SVG.

For GitHub Pages: Settings → Pages → deploy from branch, root folder. `index.html` at the
repo root is picked up automatically.

