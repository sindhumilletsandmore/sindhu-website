# Sindhu Millets & More™ — Website

A fully **static, client-side** bilingual (English / తెలుగు) website. No server, no build step, no database.
All ordering happens through **WhatsApp deep links** and social links, so it runs anywhere you drop the files.

## Files
```
index.html      → the whole website (HTML + CSS + JS in one file)
brand/           → product pack shots, logo, family photo (referenced by index.html)
CNAME            → your custom domain (edit this — see below)
.nojekyll        → tells GitHub Pages to serve files as-is
```

## Deploy to GitHub Pages (free hosting)

1. Create a new GitHub repository (e.g. `sindhu-website`). Public is fine.
2. Upload **everything inside this folder** to the repo root
   (so `index.html` sits at the top of the repo, with the `brand/` folder next to it).
   - Web way: repo → **Add file → Upload files** → drag the files in → **Commit**.
   - Git way: `git init` → `git add .` → `git commit -m "site"` → push to the repo.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
   Branch: **main**, folder: **/(root)** → **Save**.
5. Wait ~1 minute. Your site goes live at `https://<your-username>.github.io/<repo>/`.

## Custom domain

1. Buy a domain (GoDaddy, Namecheap, Google Domains, etc.).
2. Edit the **CNAME** file in this folder — replace `www.yourdomain.com` with your real
   domain (e.g. `www.sindhumilletsandmore.com`). Commit the change.
   - Or leave CNAME out and set the domain in **Settings → Pages → Custom domain** (GitHub creates CNAME for you).
3. At your domain registrar, add DNS records:
   - For **www** subdomain → a **CNAME** record pointing to `<your-username>.github.io`
   - For the **apex/root** domain (yourdomain.com) → four **A** records:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
4. Back in **Settings → Pages**, tick **Enforce HTTPS** once the certificate is issued (can take up to ~24h).

## Editing content later

Open `index.html` in any text editor:
- **Products, prices, descriptions** → the `PRODUCTS` array near the bottom `<script>`.
- **WhatsApp number** → the `WA` variable at the top of the script (`917995629557`).
- **English/Telugu text** → the `I18N` object (`en` and `te` blocks).
- **Testimonials** → the `TESTI` array (edit or replace with real customer quotes).

## Notes
- Prices are set for **Multi Millet Java Powder** and **Ragi Java Powder**; other products show
  “Price on enquiry” until you add prices in the `PRODUCTS` array.
- Fonts load from Google Fonts (needs internet — fine for any hosted site).
- WhatsApp / Instagram / Facebook / YouTube / email / call / map links are all live.
