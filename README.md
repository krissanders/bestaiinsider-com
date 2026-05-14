# bestaiinsider.com

Static landing page for Best AI Insider — the customer-facing audit-subscription product layered on top of [krissanders/ai-visibility-mcp](https://github.com/krissanders/ai-visibility-mcp).

## What's here

- `index.html` — single-page landing with pricing tiers (Free / Pro $99 / Agency $499) + email-capture form
- `robots.txt` — explicitly allows all 22 AI bots (eats own dogfood)
- `llms.txt` — LLM-friendly description per the emerging convention
- `sitemap.xml` — one URL, but present so the audit doesn't ding the site

## Deployment

Drag the directory to any static host. Cloudflare Pages, Netlify, GitHub Pages, S3, anywhere.

Before deploy:
1. Replace `https://formspree.io/f/REPLACE_ME` in `index.html` with your real Formspree (or alternative) endpoint
2. Wire `hello@bestaiinsider.com` to your real inbox (Apple Hide My Email, Gmail alias, ImprovMX, etc.)
3. Point `bestaiinsider.com` DNS at the host
4. Run `audit_ai_visibility(domain="bestaiinsider.com")` via the OSS engine — should score ≥95 (we're our own first customer)

## Status

v0.1 — landing copy + structure. No backend yet (Formspree handles email capture). When first 10 signups land via cold acquisition, build the actual report generator + Stripe checkout.
