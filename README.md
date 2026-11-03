# Kernel site (OAuth consent-screen pages)

- `index.html` - home page: describes the app, links the policy and terms (not a login page).
- `privacy.html` - privacy policy, dated 2 November 2026.
- `terms.html` - short terms of service.
- `logo-120.png` (120x120, for Google's consent screen), `logo-512.png`, `favicon.ico` - the Kernel hexagon mark.
- `make_assets.py` - regenerates the three image files (needs Pillow). `_shots/` - local screenshots, do not publish.

## Host on GitHub Pages
1. Create a public repo (e.g. `kernel-site`) and push the files above (leave out `_shots/` and `make_assets.py` if you like).
2. Repo Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
3. The site is at `https://<user>.github.io/kernel-site/`. For a domain without a path, name the repo `<user>.github.io`.

## Host on Cloudflare Pages
1. Cloudflare dashboard > Workers & Pages > Create > Pages > Upload assets (direct upload).
2. Name the project `kernel`, drag in this folder, Deploy.
3. The site is at `https://kernel.pages.dev/` (the name may differ if taken).

## Google Auth Platform > Branding
- Application home page: `https://<host>/` (or `/index.html`)
- Privacy policy link: `https://<host>/privacy.html`
- Terms of service link: `https://<host>/terms.html`
- Logo: upload `logo-120.png`.
- Put the domain (e.g. `kernel.pages.dev` or `<user>.github.io`) under Authorized domains. Verify it in Google Search Console first; Google requires this before a brand review.
