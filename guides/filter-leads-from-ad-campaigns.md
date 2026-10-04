# Filter Leads from ad campaigns

About your setup\
Getting data from your ad campaigns works best if you make use of UTM tags.&#x20;

If you are not familiar or would like to learn more, please see this article: [getting started with UTM tags](../integrations/website/tracking-marketing-campaign-data-utm-tags.md)

#### Example

If you want to see only the leads coming from paid ad campaigns:

1. Open **Leads & Accounts** and add the **Utm Tags** filter (under the behavioural filters).
2. Enter the UTM value your ads use, for example `cpc` (or `paid`, `ppc`, whatever you use as `utm_medium` in your ad links). To look at one campaign, enter the campaign name you use as `utm_campaign`.
3. Add the **First Source / First Medium / First Campaign** or **Last Source / Last Medium / Last Campaign** columns to see where each lead came from. "First" is the visit that brought the lead in, "Last" is the most recent one.
4. Save the filters as a [Segment](../fundamentals/elements/segments.md), turn on a daily notification in HTML format and add your marketing team as recipients.

Google Ads clicks without UTM tags can still be recognized by their `gclid`. See [UTM tags for Google AdWords](../integrations/website/utm-tags-for-google-adwords.md).

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/59a5583a042863033a1c5f86/file-kHvJKu3Ntc.png" alt=""><figcaption></figcaption></figure>
