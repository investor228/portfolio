# Portfolio — Maksim Padleski

Personal portfolio website of a no-code developer & automation specialist
(Bubble.io, Make, n8n, AI agents).

## Tech

- Pure static HTML + CSS — no frameworks, no JavaScript, no build step
- All assets self-hosted (tool logos inlined as SVG / local files) — zero third-party requests
- Responsive layout, single page

## Security

- Strict Content-Security-Policy (`default-src 'none'`, no scripts) — set both as a
  `<meta>` tag and via [`_headers`](./_headers) for hosts that support custom headers
  (Cloudflare Pages, Netlify)
- `X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy`, `Permissions-Policy`,
  `COOP`/`CORP`, HSTS
- No secrets, no cookies, no tracking

## Run locally

Just open `index.html` in a browser — no server required.

## Deploy

Any static host works. `_headers` is picked up automatically by Cloudflare Pages
and Netlify; on GitHub Pages the `<meta>` CSP still applies.
