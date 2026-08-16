# Search1API for Factory Droid

Live web search, page retrieval, news, sitemap discovery, and trending topics
for [Factory Droid](https://docs.factory.ai) through Search1API's hosted MCP
server and research skill.

## Install

Install the plugin from this repository as a marketplace:

```bash
droid plugin marketplace add https://github.com/superagents-lab/droid-s1
droid plugin install s1@droid-s1
```

Or browse and install interactively:

```bash
droid plugin marketplace add https://github.com/superagents-lab/droid-s1
/plugins
```

Then look for **s1** under the **droid-s1** marketplace.

## Authentication

The bundled MCP server is `https://mcp.search1api.com/mcp`. When authorization
is required, Factory Droid opens the Search1API OAuth flow. Complete
authorization in the browser; do not paste credentials into a prompt.

## Capabilities

- **Search** the live web across multiple sources (Google, Bing, DuckDuckGo,
  Yahoo, X, Reddit, GitHub, YouTube, arXiv, WeChat, Bilibili, IMDb, Wikipedia)
- **Read** and summarize web pages
- **Find** current news
- **Discover** links on a site
- **Explore** GitHub and Hacker News trends

## What this plugin contains

| Component | Purpose |
|---|---|
| `mcp.json` | Connects Factory Droid to the Search1API hosted MCP server |
| `skills/search1api/SKILL.md` | Teaches Droid when and how to use search, fetch, crawl, news, sitemap, and trending tools |

This plugin contains no hooks, executable scripts, or bundled binaries. It
connects only to Search1API's hosted MCP endpoint. Search queries, requested
URLs, and tool parameters are sent to Search1API to perform the requested web
research.

## Local development

```bash
droid plugin marketplace add ./droid-s1
droid plugin install s1@droid-s1 --scope user
droid plugin list --scope user
```

Confirm `s1` appears in the installed list and the `search1api` skill is
discoverable via `/search1api`.

## Security and data

- [Privacy policy](https://blog.search1api.com/pages/privacy)
- [Terms of service](https://blog.search1api.com/pages/terms)
- [Documentation](https://www.search1api.com/docs)

## License

MIT
