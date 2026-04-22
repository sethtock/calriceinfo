# calriceinfo

Static rebuild of calriceinfo.com, extracted from the current site and localized so it can be hosted outside Webflow.

## Status

- GitHub repo: `sethtock/calriceinfo`
- Cloudflare Pages ready
- Static routes:
  - `/`
  - `/mckenzie-seed/`
  - `/terms-of-service/`

## Cloudflare Pages setup

### Option A, Git-integrated deploys, recommended

1. In Cloudflare Pages, create a new project from GitHub
2. Select `sethtock/calriceinfo`
3. Production branch: `main`
4. Framework preset: `None`
5. Build command: leave blank
6. Build output directory: `.`
7. Deploy
8. Add custom domain: `calriceinfo.com`
9. Add `www.calriceinfo.com` and redirect it to the apex if desired

### Option B, Wrangler direct upload

```bash
npm run deploy:cf
```

This uses:

```bash
npx wrangler pages deploy . --project-name calriceinfo
```

## Files added for hosting

- `_headers` for basic security headers and long cache for static assets
- `_redirects` for slash-normalized route redirects
- `robots.txt`
- `sitemap.xml`
- `package.json` with local preview and Cloudflare deploy scripts

## Local preview

```bash
npm run dev
```

Then open http://localhost:8000
