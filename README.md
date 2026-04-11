# Olostep — Web Data for OpenClaw Agents

![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-5A45FF?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJ3aGl0ZSI+PHBhdGggZD0iTTEyIDJMMiA3bDEwIDUgMTAtNS0xMC01ek0yIDE3bDEwIDUgMTAtNS0xMC01LTEwIDV6TTIgMTJsMTAgNSAxMC01Ii8+PC9zdmc+)
![Version](https://img.shields.io/badge/version-1.0.3-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Search, scrape, crawl, map, batch, and get AI answers from the live web — directly from your OpenClaw agent.

Your agent's training data goes stale. This skill gives it the current web: scrape any URL to clean markdown, search Google with structured results, crawl entire documentation sites, batch-process up to 10,000 URLs in parallel, and get AI-synthesized answers with citations.

## Install

```bash
clawhub install olostep
```

Or manually: clone this repo into your OpenClaw skills directory.

## Setup

1. Get a free API key at [olostep.com/auth](https://olostep.com/auth) (500 requests/month, no credit card)
2. Set it in your OpenClaw config:

```bash
openclaw config set skills.entries.olostep.env.OLOSTEP_API_KEY "your-key-here"
```

Or set the environment variable:
```bash
export OLOSTEP_API_KEY="your-key-here"
```

## Tools

| Tool | What it does |
|------|-------------|
| **Scrape** | Extract content from any URL as markdown, HTML, text, or JSON. Full browser rendering, anti-bot bypass, residential proxies. JS-heavy SPAs, CAPTCHAs, geo-restricted pages — handled. |
| **Search** | Structured Google search results: titles, URLs, snippets, knowledge graph, People Also Ask. |
| **Crawl** | Follow links from a starting URL and scrape every page. Great for ingesting docs sites, blog archives, product catalogs. |
| **Batch** | Scrape up to 10,000 URLs in parallel. All pages rendered concurrently with full anti-bot protection. |
| **Map** | Discover every URL on a website instantly, filterable by glob patterns and search query. |
| **Answers** | Ask a question, get an AI-synthesized answer from live web sources — with citations and optional structured JSON output. |

## When Your Agent Should Use This

**Debugging an error** — Search for the exact error message across GitHub issues and StackOverflow, then scrape the most relevant thread for the full fix.

**Writing code from docs** — Scrape the actual API documentation and write working integration code from what is really there, not from stale training data.

**Research and comparisons** — Get structured, cited answers about pricing, features, tech stacks, or market data. Define a JSON shape and get it filled with live web data.

**Ingesting a knowledge base** — Map a docs site to discover all URLs, then batch-scrape or crawl the relevant sections into clean markdown for RAG pipelines.

**Framework migration** — Scrape the migration guide and changelog, understand breaking changes, and refactor code based on real documentation.

## Example Workflows

### Research a topic
```
1. Search Google → find authoritative sources
2. Scrape the top results → get full content as markdown
3. Synthesize into a deliverable
```

### Ingest documentation
```
1. Map the docs site → discover all page URLs
2. Batch or Crawl the relevant sections
3. Retrieve clean markdown content
```

### Debug an error
```
1. Search the exact error message (in quotes)
2. Scrape the GitHub issue or StackOverflow answer
3. Apply the fix
```

### Extract structured data at scale
```
1. Map the site to find all product/listing URLs
2. Batch scrape with a parser for structured JSON
3. Process and store the results
```

## Links

- [Olostep API Docs](https://docs.olostep.com)
- [Get API Key](https://olostep.com/auth) (free, 30 seconds)
- [OpenClaw Docs](https://docs.openclaw.ai)
- [ClawHub](https://clawhub.ai)
- [Full ClawHub Plugin](https://github.com/olostep/olostep-clawhub-plugin) (13 skills + MCP server)

## License

MIT — see [LICENSE](LICENSE) for details.
