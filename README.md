# LiyoPlanet website

Four self-contained static pages — every font, image, and icon is inlined,
so there are no build steps and no external requests.

- `index.html` — landing page
- `terms.html` — Terms of Use
- `privacy.html` — Privacy Policy
- `support.html` — Support / FAQ

## Deploy to Vercel via GitHub

1. Create a new GitHub repo and push this folder to it:
   ```
   git init
   git add .
   git commit -m "LiyoPlanet website"
   git remote add origin <your-new-repo-url>
   git push -u origin main
   ```
2. In Vercel: **Add New Project** → import that GitHub repo. No framework/build
   command needed — Vercel will serve the static files as-is.
3. In the Vercel project's **Settings → Domains**, add `liyoplanet.lsquared.sa`
   and point your DNS for that subdomain (a `CNAME` record to `cname.vercel-dns.com`,
   or whatever Vercel's domain screen instructs) from wherever `lsquared.sa` is managed.
4. `vercel.json` in this folder enables clean URLs (`/terms` instead of `/terms.html`).

## Updating content later

These files were generated from a build script (colors/fonts/copy pulled from
the actual LiyoPlanet app). If you want help making edits, easiest is to come
back with the change you want rather than hand-editing the minified inline
styles/fonts directly.
