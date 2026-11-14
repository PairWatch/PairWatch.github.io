# PairWatch landing page — pairwatchalerts.com

Static one-pager (`index.html`, no build step). Deployment = GitHub Pages + the custom domain bought 2026-11-14 at Cloudflare Registrar ($11.17/yr, auto-renew OFF, WHOIS privacy on).

## Deploy checklist (once the PairWatch GitHub account exists)

1. Create a **public** repo named `pairwatch.github.io` under the PairWatch GitHub account and push these files (`index.html`, `CNAME`, `README.md`) to `main`.
2. Repo → Settings → Pages: source = `main` branch, root. The `CNAME` file in the repo root sets the custom domain to pairwatchalerts.com.
3. In **Cloudflare DNS** for pairwatchalerts.com, add (all **DNS only / grey cloud — proxy OFF**, otherwise GitHub cannot issue the HTTPS certificate):
   - A `@` → `185.199.108.153`
   - A `@` → `185.199.109.153`
   - A `@` → `185.199.110.153`
   - A `@` → `185.199.111.153`
   - CNAME `www` → `pairwatch.github.io`
4. Wait for DNS + certificate (usually minutes, can take a few hours). Then in GitHub Pages settings tick **Enforce HTTPS**.
5. Verify: https://pairwatchalerts.com and https://www.pairwatchalerts.com both load (www redirects to apex).

## After it's live

- X profile Website field → https://pairwatchalerts.com (replaces nothing yet — currently the Telegram link is in bio text; keep the Telegram link in the bio, put the site in the Website field).
- Directory submissions unlocked: Polymark.et (needs contact email — use Cloudflare Email Routing alias e.g. contact@pairwatchalerts.com forwarding to the project inbox), LaunchPoly (place their badge on this page), PredictionMarket.tools (add their backlink), PolyMart.
- Update the track-record table + stats as new alerts accumulate (numbers on the page are as of 2026-11-14: 26 pairs / 11 rejected / 10 alerts).
