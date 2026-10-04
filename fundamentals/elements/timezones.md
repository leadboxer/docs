# Time zones

Each dataset has its own time zone. LeadBoxer uses it to show dates and times for that dataset and to decide what periods such as "Today" or "Last 7 days" mean when you filter leads and accounts. The default is Europe/Amsterdam.

Set the time zone to where your team works, or where most of your visitors are, so that "today" in LeadBoxer matches your working day.

## How to change a dataset's time zone

1. Open **Settings** in the left menu.
2. Go to **TimeZones** (Manage Dataset Timezones).
3. Every dataset you have access to is listed by name. Pick the time zone for each one from the drop-down.
4. Click **Save**.

{% hint style="info" %}
Using the [API](../../developers-and-api/developer-portal.md)? Pass the `timeZone` parameter (for example `Europe/London`) to control how time filters are evaluated in API results.
{% endhint %}
