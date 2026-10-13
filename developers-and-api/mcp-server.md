# MCP Server for AI Assistants

The LeadBoxer MCP server lets AI assistants such as Claude, Claude Code and Cursor look up companies and contacts with your LeadBoxer account. Ask "Who is behind IP 193.8.9.0?", "Enrich acme.com" or "Who is jane.doe@acme.com?" and the assistant calls LeadBoxer for you.

| Tool                 | What it does                                                                                       | Credits |
| -------------------- | -------------------------------------------------------------------------------------------------- | ------- |
| `lookup_ip`          | Identifies the company behind an IP address: organisation, domain, ISP, usage type and location     | 20      |
| `lookup_domain`      | Enriches a company domain with firmographics: industry, employees, description, address and LinkedIn | 10      |
| `lookup_email`       | Finds the professional profile behind a work email: name, headline, LinkedIn, seniority, location and work history | 50 per profile found, none if no one is found |
| `get_credit_balance` | Shows your remaining credits                                                                       | Free    |

All tools are read-only: they never change data in your LeadBoxer account. Lookups use the same credits as the App.

### Connect it

You need your LeadBoxer API key, from [Integrations → Data → API key](https://app.leadboxer.com/integrations-connectors/data/api-key) in the App. The server address and step-by-step setup for Claude, Claude Code, ChatGPT, Cursor, VS Code and other clients are on the developer portal: [LeadBoxer MCP server](https://developers.leadboxer.com/docs/mcp).

Read more about what you can do with it on [leadboxer.com/mcp](https://www.leadboxer.com/mcp).
