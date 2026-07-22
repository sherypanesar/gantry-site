# Gantry — marketing site

Single-page marketing site for Gantry. This is the **"link home"** referenced in the
content calendar (Week 0): the destination for the Product Hunt link, link-in-bio, and the
SEO articles. Fully self-contained (one `index.html` + `img/`), dark-themed to match the app.

## What's here
- `index.html` — the landing page (hero, wedge, features, connect, gallery, YouTube demo,
  pricing, FAQ, CTAs). Responsive; light/dark not needed (brand is dark-only).
- `img/` — icon, feature graphic (used as the OG/social share image), and 6 app screenshots.

## How to publish (free, GitHub Pages — same as the privacy site)

Option A — add it to the existing `gantry-legal` Pages repo:
1. Copy `index.html` and `img/` into that repo (e.g. under a `/site` path, or the root if you
   want it to be the repo's main page).
2. Push. GitHub Pages serves it at `https://sherypanesar.github.io/<repo>/`.
3. Update the `<link rel="canonical">` and OG URLs in `index.html` to the final address.

Option B — a dedicated `gantry` repo:
1. Create a public repo named `gantry`, drop these files in the root, enable Pages
   (Settings → Pages → deploy from `main`/root).
2. Site goes live at `https://sherypanesar.github.io/gantry-site/` (already set as the canonical URL).

> A custom domain (e.g. `gantry.app`) can be pointed at Pages later via a `CNAME` file.

## Notes
- The **YouTube embed** shows an error when opened as a local `file://` — that's a browser
  origin restriction, not a bug. It works once served over `https://` (GitHub Pages).
- All Play links carry UTM `referrer` params (`utm_source=site`) so installs from the site
  show up in Play Console acquisition reports.
- Pack prices in the pricing section mirror `frontend/src/lib/entitlements.ts`. If you change
  prices in Play/console, update them here too.
