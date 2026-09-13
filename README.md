# Daily Gaming Pack — @augmc2

A personalized daily gaming news digest, tuned to @augmc2's own posting history rather than generic "everything gaming" coverage.

## What's here
- `index.html` — the digest UI (installable as a home-screen web app via `manifest.json` + `sw.js`).
- `data/YYYY-MM-DD.json` — one file per day, containing ranked items (headline, "why you care" hook, summary, key facts, official source image + credit, source links).
- `images/official/` — real, downloaded (not AI-generated) press images from official publishers/outlets, resized/compressed for fast mobile loading. Each is credited on-card.

## How personalization works
See `profile-augmc2.md` and `coverage-log.md` in this automation's persistent memory for the full ranking rules and a log of previously-covered headlines (used to avoid repeating stories).

## Delivery limitation
This automation has no linked repository or hosting/deploy credentials, so there's no permanently-hosted URL. Each session, the app is rebuilt fresh in the run's ephemeral workspace and exposed via a temporary Cloudflare quick tunnel (`cloudflared tunnel --url ...`) for phone access. That tunnel dies when the session ends — it is NOT persistent across the daily cron trigger. For a permanent link, connect a real host (GitHub Pages/Vercel/Netlify) via Cursor secrets.
