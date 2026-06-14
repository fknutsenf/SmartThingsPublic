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

## Deploy (Vercel)

This is a static site, so Vercel serves it with no build step.

1. In Vercel, **Add New… → Project** and import this GitHub repo.
1. **Framework Preset:** `Other`. Leave Build Command and Output Directory empty;
   Root Directory `./`. Click **Deploy**.
1. Every push to the default branch then triggers a new deployment automatically.

### Custom domain: fredheimlogistics.com

1. In the Vercel project: **Settings → Domains** and add `fredheimlogistics.com`
   and `www.fredheimlogistics.com` (set `www` to redirect to the apex).
1. Vercel shows the exact DNS records to add at your DNS host — follow that screen.
   Typically the apex `@` points to an A record `76.76.21.21` and `www` to a
   `*.vercel-dns.com` CNAME.
1. Vercel auto-issues HTTPS once the domain verifies.

## Before going live

- Replace the placeholder email `contact@fredheim.com` (appears in the nav, contact
  link, and form handler).
- The contact form opens the visitor’s mail client (no backend). For real lead
  capture, wire it to Formspree, a Netlify form, or a serverless function.
- Add analytics, favicon, and Open Graph / meta tags as needed.

## Files

- `index.html` — the site (served at the root)
- `fredheim.html` — identical copy under the original filename
