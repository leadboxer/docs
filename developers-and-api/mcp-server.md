# MCP Server for AI Assistants

The LeadBoxer MCP server lets AI assistants such as Claude, Claude Code and Cursor look up companies with your LeadBoxer account. Ask "Who is behind IP 193.8.9.0?" or "Enrich acme.com" and the assistant calls LeadBoxer for you.

| Tool                 | What it does                                                                                       | Credits |
| -------------------- | -------------------------------------------------------------------------------------------------- | ------- |
| `lookup_ip`          | Identifies the company behind an IP address: organisation, domain, ISP, usage type and location     | 20      |
| `lookup_domain`      | Enriches a company domain with firmographics: industry, employees, description, address and LinkedIn | 10      |
| `get_credit_balance` | Shows your remaining credits                                                                       | Free    |

All tools are read-only: they never change data in your LeadBoxer account. Lookups use the same credits as the App.

### Connect it

You need your LeadBoxer API key, from [Integrations → Data → API key](https://app.leadboxer.com/integrations-connectors/data/api-key) in the App. The server address and step-by-step setup for Claude, Claude Code, Cursor and other clients are on the developer portal: [Connect LeadBoxer to Claude](https://developers.leadboxer.com/docs/connect-leadboxer-to-claude).

Read more about what you can do with it on [leadboxer.com/mcp](https://www.leadboxer.com/mcp).
