# MCP Server for AI Assistants

The LeadBoxer MCP server lets AI assistants such as Claude, Claude Code and Cursor look up companies with your LeadBoxer account. Ask "Who is behind IP 193.8.9.0?" or "Enrich acme.com" and the assistant calls LeadBoxer for you.

The server runs at:

```
https://mcp.leadboxer.com/mcp
```

***

### What it can do

| Tool                 | What it does                                                                                       | Credits |
| -------------------- | -------------------------------------------------------------------------------------------------- | ------- |
| `lookup_ip`          | Identifies the company behind an IP address: organization, domain, ISP, usage type and location     | 20      |
| `lookup_domain`      | Enriches a company domain with firmographics: industry, employees, description, address and LinkedIn | 10      |
| `get_credit_balance` | Shows your remaining credits                                                                       | Free    |

All tools are read-only: they never change data in your LeadBoxer account.

### Before you start

You need your LeadBoxer API key. Find it in LeadBoxer under [Integrations → API key](https://app.leadboxer.com/integrations-connectors/data/api-key).

### Connect in Claude

1. In Claude, open **Settings → Connectors**.
2. Click **Add custom connector**, name it "LeadBoxer" and enter `https://mcp.leadboxer.com/mcp`.
3. Click **Connect**. A LeadBoxer page opens.
4. Paste your API key and click **Connect**. You're returned to Claude.

Turn on LeadBoxer in a chat's tools menu and ask something like "How many LeadBoxer credits do I have left?".

Your API key stays with LeadBoxer: Claude only receives a token that lets it call the tools.

### Claude Code, Cursor and other clients

For Claude Code, run:

```bash
claude mcp add --transport http leadboxer https://mcp.leadboxer.com/mcp
```

Then run `/mcp` and choose LeadBoxer to connect. Other MCP clients that support remote servers can use the same URL.

### Example prompts

* "Who is behind IP 193.8.9.0?"
* "Enrich acme.com with company details."
* "Here's my server access log. Which companies visited, ranked by employee count?"

***

For full setup instructions, headers for scripts and troubleshooting, see [Connect LeadBoxer to Claude](https://developers.leadboxer.com/docs/connect-leadboxer-to-claude) on the Developer Portal.
