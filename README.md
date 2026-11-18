# Security Guard Deployment Status · Shadowfax

A single-file HTML dashboard comparing current (latest) security-guard deployment
against the required optimum per site, with NCR and South zone-deployment views
and a parameter-based optimum calculator.

## Contents

| File | Purpose |
| --- | --- |
| `index.html` | The entire dashboard — self-contained (data embedded, Shadowfax theme inline). |
| `vercel.json` | Optional static-site config (clean URLs). |
| `.gitignore` | Standard ignores. |

No build step, no dependencies to install. The only external request is the
SheetJS library loaded from a CDN (used for the drag-drop refresh); it loads at
runtime and needs no setup.

## Deploy on Vercel

1. **Create a GitHub repo** and upload these three files to the repository root
   (`index.html`, `vercel.json`, `README.md`). `index.html` must sit at the root.
2. Go to **vercel.com → Add New → Project → Import** the GitHub repo.
3. **Framework Preset: Other.** Leave Build Command and Output Directory empty
   (it is a static site). Click **Deploy**.
4. Vercel returns a live URL. Every push to the repo redeploys automatically.

## Updating the data

The site data is embedded in `index.html`. To refresh it, replace `index.html`
with a newly built version and push — the deploy updates on push.
