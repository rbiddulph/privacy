# Cloudflare Pages deployment

The MCFCBot legal site is a static Cloudflare Pages project connected to `rbiddulph/privacy`.

Use these build settings:

- Production branch: `master`
- Build command: `exit 0`
- Build output: `public`
- Root directory: leave blank
- Build cache: optional
- Environment variables: none

The build output setting is important: Pages must upload `public/`, not the repository root. Automatic production deployments can remain disabled when releases should be manual.

The expected policy paths are:

- `/matchday/privacy/`
- `/matchday/terms/`
- `/moderation/privacy/`
- `/moderation/terms/`

The site is intentionally static. `public/_headers` supplies its security headers. Do not add analytics, cookies, forms, third-party fonts or client-side scripts without first updating the relevant privacy disclosures and security headers.
