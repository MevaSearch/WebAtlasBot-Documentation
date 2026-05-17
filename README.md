# [MevaSearch](https://mevasearch.com/) — ACTIVE CRAWLER

## Meet WebAtlasBot

The official search engine crawler for MevaSearch, building a safe and filter-free map of the internet.

---

## Identification

Our bot uses the following User-Agent string:

```
WebAtlasBot/2.0 (+https://mevasearch.com/bot)
```

Always verify the bot via reverse DNS to ensure the request originates from MevaSearch infrastructure.

---

## Behavior

WebAtlasBot is designed to maintain a minimal load on web servers:

- Respects `robots.txt` directives (`Disallow`, `Allow`).
- Supports `Crawl-delay` to prevent server strain.
- Verifies `noindex` and `canonical` tags.
- Uses adaptive crawling — automatically slows down based on your server's response times.

---

## WebAtlas Index

All crawled content is processed and stored in the **WebAtlas Index** — our proprietary global database designed for high-performance retrieval and semantic analysis.

By being part of the index, your site becomes discoverable through our search infrastructure, reaching researchers, developers, and educators looking for high-quality technical content.

---

## Crawl Control

### Restrict specific directories

```
User-agent: WebAtlasBot
Disallow: /private/
Disallow: /admin/
Disallow: /tmp/
```

### Block the bot completely

```
User-agent: WebAtlasBot
Disallow: /
```

### Allow full access

```
User-agent: WebAtlasBot
Allow: /
```

### Throttle crawling speed

```
User-agent: WebAtlasBot
Crawl-delay: 10
```

### Per-page control via HTML meta tags

If you cannot modify `robots.txt`, add the following tag to the `<head>` section of any page you want excluded:

```html
<meta name="robots" content="noindex">
```

---

## Why Are We Visiting?

WebAtlasBot collects data to power the MevaSearch engine. We focus on high-quality, educational, and technical content. Our goal is not aggressive indexing, but rather creating a knowledge base resistant to algorithmic manipulation — a filter-free, semantic map of the internet's most valuable information.

---

## Contact

Questions, feedback, or specific crawling requirements?

- **Email:** bot[at]mevasearch.com
- **Website:** [mevasearch.com](https://mevasearch.com)
- **Developer:** [WebOrbiton Team](https://weborbiton.com)

---

*© 2026 MevaSearch. All rights reserved.*
