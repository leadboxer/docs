# Leadscore

Lead Scoring is a powerful concept making its way to the top of everyone’s mind in the Lead Generation space. Now that you are collecting data, it’s time to set custom, automatically calculated lead scoring.

We calculate each leads score 'on-the-fly', which means every time you open a report we (re)calculate the score based on the scoring algorithm you have set. \
\
This powerful tool means that we show you the most qualified and interesting leads at the top of the list.&#x20;

### Set your Leadscore

Once you start using LeadBoxer, you'll notice that every lead has a Leadscore. By default, your leads are sorted based on a standard Leadscore setting. Now is the time to give it your personal touch. If you are unsure how to start, you can select one of our predefined settings, and adjust them based on your needs. To do this, just go to the leadscore page.

Click below and jump to our Leadscore management guide

{% content-ref url="../../guides/how-to-set-your-leadscore.md" %}
[how-to-set-your-leadscore.md](../../guides/how-to-set-your-leadscore.md)
{% endcontent-ref %}

## Technical API section:

### Leadscore parameters

If you want to use the leadscore features build inside our API you can use this documentation to get started.

The LeadBoxer scoring engine can score on 4 criteria

1. Range
2. Match
3. Exist
4. Boost

### Range

A range can be used for scoring on number ranges, eg pageviews, visits, etc.Range needs these 5 values:

1. field name
2. Start of the range
3. End of range
4. Score value
5. Comma (not for last)

**Example:**

{% code overflow="wrap" %}
```
user.total_number_visits.total_number_visits_long|1|5|2.3,user.total_number_visits.total_number_visits_long|5|25|4.7,user.total_number_visits.total_number_visits_long|25|1000|7.0,user.total_pages_viewed.total_pages_viewed_long|1|5|2.3,user.total_pages_viewed.total_pages_viewed_long|5|25|4.7,user.total_pages_viewed.total_pages_viewed_long|25|1000|
```
{% endcode %}

### Match

Match can be used if you want to score on a exact value match on any field

A match needs 3 values

1. field name
2. Value
3. Score

**Example**

```
OrganizationIndustry|Publishing|9|last_country_code|US|9
```

### Exists

Exist can be used to score on the existence of a value

An Exist needs 2 values

1. field name
2. Score

**Example**

```
email|3,organizationPhone|10,organizationDomain|15
```

### Boost

Boost can be used for scoring on events/pageviews/etcA Boost requires 3 values

1. Event type (usually root\_url)
2. The actual URL
3. Score

**Example**

{% code overflow="wrap" %}
```
root_url|https://mydomain.com/contact/|7,root_url|https://mydomain.com/buy-your-equipment/|7,root_url|https://mydomain.com/sell-your-equipment/|7
```
{% endcode %}
