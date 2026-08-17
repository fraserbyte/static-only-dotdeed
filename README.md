# DOT DEED — Landing Site (static)

A static, no-backend version of DOT DEED for **GitHub Pages** — built to satisfy Stripe's
business-website requirement and as a lightweight marketing/demo site.

## What's here

- **`index.html`** — a single-page landing with:
  - Brand hero + features + pricing
  - **Interactive certificate demo** (design + download PNG — fully client-side)
  - **Replicated Domain Shopper** — same look & feel, but backed by **demo data** (no live Name.com API)
  - Contact CTA
- **`favicon.png`**, **`image.png`** — brand assets

## Run locally

```bash
# Option 1 — just open the file
open index.html

# Option 2 — local static server
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new **empty** GitHub repo, e.g. `fraserbyte/dotdeed-landing`.
2. Push this folder to it:
   ```bash
   git init
   git add -A
   git commit -m "Initial static landing"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/dotdeed-landing.git
   git push -u origin main
   ```
3. Enable Pages: repo **Settings → Pages → Source: Deploy from a branch → `main` → `/ (root)`**.
4. Your site is live at `https://YOUR_USERNAME.github.io/dotdeed-landing/` after ~1–2 min.

### Optional — custom subdomain (nicer for Stripe)
- Add a `CNAME` file containing e.g. `landing.dotdeed.com`
- Add a DNS `CNAME` record `landing` → `YOUR_USERNAME.github.io`
- Set the custom domain in repo **Settings → Pages**

## Notes

- **No backend** — the certificate demo and domain shopper are 100% client-side.
- **Demo data** — domain availability/pricing shown are examples, not live registrations.
- Ordering on this site is intentionally **not available** (it's for verification/marketing);
  the full app handles real checkout.
