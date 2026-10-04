# Developers & API

LeadBoxer App is built on the **LeadBoxer Platform**: the same tracking, identification and enrichment, available through APIs for your own products, websites and workflows. Developer documentation lives on [developers.leadboxer.com](https://developers.leadboxer.com); this page only covers what you need from the App.

***

### The three APIs

* **Track API**: send website, server-side and email events into LeadBoxer.
* **Lookup API**: identify the company behind an IP address, or enrich a company domain.
* **App API**: read your leads and accounts, and manage tags, owners, segments, datasets and users.

See [When to use which API](https://developers.leadboxer.com/docs/when-to-use-which-api) for details.

### Get your API key

API keys are generated from your LeadBoxer account:

1. Log in to [LeadBoxer App](https://app.leadboxer.com). No account yet? [Create a free one](https://app.leadboxer.com/sign-up).
2. Go to [Integrations → Data → API key](https://app.leadboxer.com/integrations-connectors/data/api-key).
3. Copy the key and send it in the `x-api-key` header of every request.

{% hint style="warning" %}
Treat your API key like a password. Never put it in your website's JavaScript or in a public repository: call the API from your server instead.
{% endhint %}

API calls that identify or enrich data use the same credits as the App. The first 25,000 credits each month are free. See [LeadBoxer for developers](https://www.leadboxer.com/developers) and [pricing](https://www.leadboxer.com/pricing).

### Useful links

* [Quickstart](https://developers.leadboxer.com/docs/quickstart)
* [API reference](https://developers.leadboxer.com/reference)
* [Credit cost per endpoint](https://developers.leadboxer.com/docs/credit-usage-cost-model) and [rate limits](https://developers.leadboxer.com/docs/credits-rate-limits)
* [API changelog](https://developers.leadboxer.com/changelog)
* [MCP server for AI assistants](mcp-server.md)
* [n8n and Make automation](https://www.leadboxer.com/integrations/automation), plus our guides for [Zapier](../integrations/other/how-to-get-started-with-leadboxer-on-zapier/README.md), [make.com](../integrations/other/make.com.md) and [n8n](../integrations/other/n8n.md)
