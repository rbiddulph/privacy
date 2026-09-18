# Cloudflare Workers static-site deployment

This repository contains legacy app policies at its root and a separate static legal site in public/ for the MCFCBot Devvit apps. Cloudflare's current repository-import flow deploys this as a Worker with Static Assets.

On the Set up your application screen, use:

- Repository: rbiddulph/privacy
- Production branch: master
- Build command: leave blank
- Builds for non-production branches: off unless preview builds are wanted
- Protect with Cloudflare Access: off
- Root directory: leave blank
- Deploy command: leave the default npx wrangler deploy
- Token: create automatically
- Variables: none

The committed wrangler.jsonc names the Worker mcfcbot and serves the public/ directory. The small server-side Worker adds security headers; it does not use cookies, analytics, forms or client-side scripts.

The expected policy paths are:

- /matchday/privacy/
- /matchday/terms/
- /moderation/privacy/
- /moderation/terms/

The site is intentionally static. Do not add analytics, cookies, forms, third-party fonts or client-side scripts without first updating the relevant privacy disclosures and security headers.
