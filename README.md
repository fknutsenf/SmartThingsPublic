# Fredheim Logistics

Marketing site for Fredheim Logistics — outsourced commercial freight management
for cargo owners and industrial shippers (ocean · barge · inland).

Single self-contained static page. No build step, no dependencies.

## Run locally

Open `index.html` in any browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (GitHub Pages)

Deployment is automated via GitHub Actions (`.github/workflows/deploy-pages.yml`).

1. In the repo, go to **Settings → Pages → Build and deployment → Source: GitHub Actions**.
1. Push to `master` (or `main`), or run the **Deploy to GitHub Pages** workflow
   manually from the **Actions** tab.
1. Site goes live at `https://<your-username>.github.io/<repo-name>/`.

## Before going live

- Replace the placeholder email `contact@fredheim.com` (appears in the nav, contact
  link, and form handler).
- The contact form opens the visitor’s mail client (no backend). For real lead
  capture, wire it to Formspree, a Netlify form, or a serverless function.
- Add analytics, favicon, and Open Graph / meta tags as needed.

## Files

- `index.html` — the site (served at the root by GitHub Pages)
- `fredheim.html` — identical copy under the original filename
