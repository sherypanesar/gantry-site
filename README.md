# Gantry — marketing site

**🟢 LIVE at https://sherypanesar.github.io/gantry-site/** (published 2026-07-23).

Single-page marketing site for Gantry + the guides blog. This is the **"link home"** for the
Product Hunt link, link-in-bio, and the SEO articles. Self-contained, dark-themed to match the app.

## What's here
- `index.html` — the landing page (hero, wedge, features, connect, gallery, YouTube demo,
  pricing, FAQ, CTAs, a "Guides" link).
- `blog/` — `index.html` guides index + 4 SEO article pages (converted from
  `docs/marketing/articles/`).
- `img/` — icon, feature graphic (OG/social image), and 6 app screenshots.

## How it's published
It lives in a **dedicated public repo** `sherypanesar/gantry-site` (the private app repo
already owns the `gantry` name), with **GitHub Pages** serving `main` / root. The site source
of truth stays here in `cnc-control/marketing-site/`; it was published as that repo's root via
`git subtree`.

## To update the live site
1. Edit files here, commit to `cnc-control`.
2. From the repo root, push the subfolder up:
   ```bash
   git subtree push --prefix=marketing-site https://github.com/sherypanesar/gantry-site.git main
   ```
3. GitHub Pages rebuilds in ~1–2 min. (Check: `gh api repos/sherypanesar/gantry-site/pages/builds/latest --jq .status`.)

## Notes
- Canonical + OG URLs point at `https://sherypanesar.github.io/gantry-site/`.
- A custom domain (e.g. `gantry.app`) can be added later via a `CNAME` file + DNS.
- All Play links carry UTM `referrer` params (`utm_source=site`) so installs show in Play
  Console acquisition reports.
- Pack prices in the pricing section mirror `frontend/src/lib/entitlements.ts` — update here if
  they change in Play.
