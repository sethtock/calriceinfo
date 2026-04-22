# calriceinfo

Static rebuild of calriceinfo.com, extracted from the current site and localized so it can be hosted outside Webflow.

## Deploy recommendation

Use Cloudflare Pages:

1. Connect this repo in Cloudflare Pages
2. Framework preset: None
3. Build command: leave blank
4. Build output directory: /
5. Set custom domain: calriceinfo.com

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000
