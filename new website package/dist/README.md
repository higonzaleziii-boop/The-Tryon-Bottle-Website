# The Tryon Bottle — Netlify Deploy

Static single-page site. Fully self-contained (all images embedded; only Google Fonts load from a CDN).

## Option A — Drag & drop (fastest)
1. Go to https://app.netlify.com/drop
2. Drag this **entire folder** onto the page.
3. Netlify gives you a live URL instantly. Done.

## Option B — Netlify CLI
```
npm install -g netlify-cli
netlify deploy --dir . --prod
```

## Option C — Git / continuous deploy
1. Push this folder to a GitHub repo.
2. In Netlify: "Add new site" → "Import an existing project" → pick the repo.
3. Build command: (leave blank). Publish directory: `.`
4. Deploy.

## Custom domain
After deploy: Site settings → Domain management → Add your domain (e.g. thetryonbottle.com) and follow the DNS steps.

## Files
- `index.html` — the website
- `netlify.toml` — publish dir + basic security headers
