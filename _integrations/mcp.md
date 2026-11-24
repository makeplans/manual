---
title: "MCP for AI assistants"
description: "Connect an AI assistant such as Claude to your MakePlans account with MCP."
nav_order: 19
verified: 2026-11-23
review: needs-espen
---

# MCP for AI assistants

With MCP (Model Context Protocol), an AI assistant such as Claude can work with your MakePlans account. It can check availability, list reservations and events, look up customers, and create or cancel reservations.

## Set it up

1. Enable the API. See [Enable the API](/integrations/api/). The assistant logs in with your API key.
2. Open setup and select **Developer**, then **MCP - AI assistants**.
3. Follow the [MCP guide](https://developer.makeplans.com/guide/mcp/) to connect your assistant.

{% include alert.html type="warning" content="An assistant connected this way can read customer data and change reservations. Connect only assistants you trust." %}
