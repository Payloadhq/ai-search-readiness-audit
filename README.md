# AI Search Readiness Audit

A one-click Chrome extension (Manifest V3) that audits any page against the documented technical gates deciding whether AI engines can see, read, and cite it.

By **Payload** — *small software that earns its keep.*

## The problem

Your content ranks on Google but ChatGPT never cites it. Perplexity doesn't mention you. AI search engines are becoming a major discovery channel, and most sites are technically invisible to them — not because the content is bad, but because of technical barriers nobody checked.

## What it checks

1. **Raw-HTML coverage** — Measures what fraction of the rendered page's words exist in the raw HTML, plus which H1s, H2s, JSON-LD blocks, title, canonical, and robots meta are missing from raw HTML. AI crawlers (GPTBot, PerplexityBot, ClaudeBot, …) fetch pages without executing JavaScript, so content that only appears after JS runs is invisible to them.
2. **AI Overviews eligibility** — Reads the meta robots tag, `X-Robots-Tag` header, and `data-nosnippet` usage. Reports whether any directive blocks the page from Google's AI Overviews, citing the exact directive.
3. **AI-crawler robots.txt matrix** — Parses the site's live robots.txt and shows which known AI crawlers are allowed, blocked, or unmentioned.
4. **Dead schema detector** — Extracts JSON-LD `@type`s and flags types Google has retired or limited.

Every verdict cites the underlying documentation or measured behavior. No invented "AI visibility score." No ranking predictions. No SEO advice.

**100% client-side:** no accounts, no servers, no data leaves the browser.

## How it works

1. Install the extension (load unpacked in Chrome, Edge, or Brave).
2. Navigate to any page.
3. Click the extension icon.
4. Get pass / warn / fail for each check with plain-English explanations.

## Get the extension

This repo contains documentation. The full extension ($59, one-time) includes:

- Chrome extension source (Manifest V3, no build step)
- Install and usage guide
- Lifetime updates

**Buy:** [Gumroad](https://payloadtools.gumroad.com/l/ai-search-readiness-audit) · [Whop](https://whop.com/payload-f126/products/ai-search-readiness-audit-chrome-extension/)

7-day refund if the product is materially not as described or cannot be made functional after reasonable support.

## Support

kyler.simmons.partners@gmail.com

Telegram: https://t.me/payloadtool
Patreon: https://patreon.com/PayloadTools
