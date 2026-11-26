---
name: datacircle
description: Find the best or cheapest GTM API plan (an email finder, company enrichment, phone validation, web search and so on) with Datacircle's list_apis and search_plans tools. Use it when the user asks which provider or plan to pick for one of these APIs, or what one costs.
---

# Datacircle

The `datacircle` MCP server gives two tools on Datacircle's sheet of GTM APIs (https://datacircle.dev):

- `list_apis`: every API on the sheet, with how many plans and providers it has. Call it first when you don't know an API's name.
- `search_plans`: the plans of one API or of every API, best first by score. Pass the API's name from `list_apis` as `api` and a provider or plan name as `query`. Leave `sort` out for the best plans; pass `sort` `price` only when the user asks for the cheapest.

Call `list_apis` for the API's name, then `search_plans` with it. Give each plan's provider, score, price per 1,000 and its page on datacircle.dev.
