# Developers & API

LeadBoxer has an API for developers who want to use LeadBoxer data in their own products, websites or workflows. Full documentation, guides and the API reference are on the [LeadBoxer Developer Portal](https://developers.leadboxer.com/).

***

### What you can do with the API

* **Look up companies:** identify the company behind an IP address, or enrich a company domain with firmographic data.
* **Read your leads:** get leads, lead details, sessions and events, or export leads as CSV.
* **Manage your account:** set lead tags, assign leads, and manage segments, datasets and users.
* **Send events:** track website or server-side events and email opens and clicks.

### Get your API key

1. Log in to [LeadBoxer](https://app.leadboxer.com).
2. Go to [Integrations → API key](https://app.leadboxer.com/integrations-connectors/data/api-key).
3. Copy your API key and send it in the `x-api-key` header of every request.

```bash
curl "https://api.leadboxer.com/v1/domain-lookup?domain=leadboxer.com" \
  -H "x-api-key: YOUR_API_KEY"
```

{% hint style="warning" %}
Treat your API key like a password. Never put it in your website's JavaScript or in a public repository: call the API from your server instead.
{% endhint %}

### Credits and rate limits

API calls that identify or enrich data use credits, the same as in the app. For example an IP lookup uses 20 credits and a domain lookup 10 credits. See [LeadBoxer Credits](../fundamentals/elements/leadboxer-credits.md) and [Pricing Explained](../fundamentals/leadboxer-pricing-explained.md).

Requests are also limited per minute per endpoint. See [Rate limiting](https://developers.leadboxer.com/docs/credits-rate-limits) for the limits.

### Useful links

* [Quickstart](https://developers.leadboxer.com/docs/quickstart)
* [API reference](https://developers.leadboxer.com/reference)
* [Authentication & API keys](https://developers.leadboxer.com/docs/authentication-api-keys)
* [API changelog](https://developers.leadboxer.com/changelog)
* [MCP server for AI assistants](mcp-server.md)
* [Zapier](../integrations/other/how-to-get-started-with-leadboxer-on-zapier/README.md), [make.com](../integrations/other/make.com.md) and [n8n](../integrations/other/n8n.md) for no-code workflows
