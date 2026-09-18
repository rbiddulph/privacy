# Cloudflare Pages deployment

This repository contains legacy app policies at its root and a separate static legal site in public/ for the MCFCBot Devvit apps.

Configure Cloudflare Pages with:

- Repository: rbiddulph/privacy
- Production branch: master
- Framework preset: None
- Build command: leave blank
- Build output directory: public
- Suggested project name: mcfcbot-legal

The expected policy paths are:

- /matchday/privacy/
- /matchday/terms/
- /moderation/privacy/
- /moderation/terms/

The site is intentionally static. Do not add analytics, cookies, forms, third-party fonts or client-side scripts without first updating the relevant privacy disclosures and security headers.
