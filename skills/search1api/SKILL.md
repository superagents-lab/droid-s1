---
name: search1api
description: Live web search, page retrieval, news, sitemap discovery, and trending topics through Search1API. Use when the user asks to search the web, research a current topic, read or summarize a URL, check recent news, explore a site's links, or investigate trending topics.
---

# Search1API

Use the bundled Search1API MCP server for live web research. Its tools may be
namespaced by the host, but their final names are `search`, `fetch`, `news`,
`crawl`, `sitemap`, and `trending`.

If the host reports that authorization is required, ask the user to complete
the host's Search1API OAuth flow. Never ask the user to paste credentials into
the conversation.

## Choose the right tool

| User intent | Tool |
|---|---|
| Search the web | `search` |
| Read a result returned by `search` | `fetch` with the result `id` |
| Read or summarize a URL | `crawl` |
| Find recent news | `news` |
| Discover links on a site | `sitemap` |
| Explore GitHub or Hacker News trends | `trending` |

## Tune the request

- Quick lookup: request about 5 results.
- Broad research: request about 15 results, then read the 3–5 strongest sources.
- Latest or recent: use an appropriate day or month time range.
- Domain-specific research: select the matching source or restrict results to
  the requested domain.
- Match an explicit result count from the user when the tool permits it.

## Research workflow

1. Search broadly enough to identify multiple independent sources.
2. Read the most relevant source pages instead of relying only on snippets.
3. Prefer primary sources for technical, legal, medical, financial, or current
   product claims.
4. Synthesize the findings and preserve the source URLs in the answer.
5. Clearly distinguish sourced facts from inference.

Do not dump raw tool output when a concise synthesis answers the question.
