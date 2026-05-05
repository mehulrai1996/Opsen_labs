# Opsen Labs — Cloudflare Pages Deployment Guide

## Files in this package

| File | Purpose |
|------|---------|
| `index.html` | Homepage |
| `mvp-sprint.html` | MVP Sprint service page |
| `mvp-recovery.html` | MVP Recovery service page |
| `product-optimization.html` | Product Optimization service page |
| `_redirects` | Cloudflare Pages redirect rules |
| `_headers` | Cloudflare Pages HTTP headers (security + caching) |

## How to deploy on Cloudflare Pages

### Option A — Drag & Drop (fastest)

1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Pages**
2. Click **Create a project** → **Direct Upload**
3. Name your project (e.g. `opsen-labs`)
4. Drag this entire folder onto the upload zone
5. Click **Deploy site** — you're live in seconds

### Option B — GitHub (recommended for ongoing updates)

1. Push all files to a GitHub repository
2. In Cloudflare Pages → **Create a project** → **Connect to Git**
3. Select your repository
4. **Build settings:**
   - Framework preset: `None`
   - Build command: *(leave empty)*
   - Build output directory: `/` (root)
5. Click **Save and Deploy**

Every push to `main` will auto-deploy.

### Custom Domain

After deploying, go to your project → **Custom domains** → Add your domain.
Cloudflare handles SSL automatically.

## Notes

- All pages are pure static HTML — no build step required
- Fonts are loaded from Google Fonts CDN (internet required)
- Forms are UI-only; connect to a form backend (Formspree, Netlify Forms, etc.) as needed
