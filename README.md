# The Avenella Agency — website

Homepage for The Avenella Agency (part of the Avenella Group). One self-contained static `index.html` with inline CSS and JS, no build step. Scroll motion is CSS scroll-driven animation plus a small inline kit; no libraries.

## Deploy (Vercel)

This repo is a static site. In Vercel:

1. **New Project → Import** `AvenellaTom/avenella-agency-site`.
2. Framework preset: **Other** (no build). Build command: none. Output directory: **/** (root).
3. Deploy. Vercel serves `index.html` at the root and redeploys automatically on every push to `main`.
4. Add the domain `avenellaagency.com` under the project's **Domains**, then point DNS at Vercel.

After that, any push to `main` goes live in under a minute. No manual cPanel uploads.

## Updating the site

Changes are made to `index.html` (and assets) and pushed to `main`. Ask and the edit is committed and pushed here; Vercel does the rest. See `AGENTS.md` for how the file is structured so edits stay safe.

## Assets

In the repo now:

- `index.html` — the site
- `hero-agency.jpg` — faded hero background
- `logo-agency-ondark.png` / `logo-agency-onlight.png` — the `avenella.agency` lockup (white / black)
- `logo-group-ondark.png` / `logo-group-onlight.png` — the `avenella.` group mark (white / black)

**Still to add** (the site references these by filename; add them to the repo root):

- Case/work images: `work-kasp.jpg`, `work-pierluigis.gif`, `work-visa.jpg`, `work-latifa.jpg`, `work-zorazenith.jpg`, `work-pthr.jpg`, `work-luxlife.jpg`, `work-nbprivate.jpg`
- Client logo strip: `client-logo-1.png` … `client-logo-22.png`
- `hero-video.mp4` — plays in the hero round circle and as the faded hero background (falls back to `hero-agency.jpg` until added)
- `og-image.jpg` (social preview), `favicon.ico` optional

Missing images fail gracefully (clean dark cards / hidden strip), so the site works before they are added.

## Forms

The contact form and newsletter post to Formspree (`formspree.io/f/xeevolwo`). Swap the endpoint in `index.html` if the form destination changes.

Google Analytics tag `G-N9EZL9GBDM` is included.
