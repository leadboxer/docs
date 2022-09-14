---
description: Formerly known as MailPlus
---

# Spotler

### 1. Track Spotler Email opens or reads:

To track mail open/reads, add a new block switch to the HTML/code view in there you need to add:

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=Voorbeeld-Campagne-Naam&email={email}"/>
```
{% endcode %}

{% hint style="info" %}
Make sure you change datasetId and campaign name in above snippet.

Unfortunatly, Spotler does not have the option to dynamically use the title of the email in the campaign variable, meaning you will need to either use a generic campaign name or manually change this for each email that is send out.
{% endhint %}

### 2. Tracking Spotler clicks

First we recommend you enable the Google Analytics integration, so that UTM tags are added to all the URLs

Secondly, you can to add identification parameters to every URL. This can be accomplished by using 'Extra parameters' feature. We recommend to add email and company parameters.

<figure><img src="../../../.gitbook/assets/Screenshot_13_09_2022__11_44.png" alt=""><figcaption></figcaption></figure>

Even though it looks like it is enabled for for all emails like this, we found It might be necessary to manually enable this again in the emails/ newsletters themselves.

&#x20;Click on the Analytics button at the top of the email

<figure><img src="../../../.gitbook/assets/Spotler (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Spotler.png" alt=""><figcaption></figcaption></figure>

The Extra parameters feature only allows for 2 additional parameters, so if you need more you can still manually add them like this:

{% code overflow="wrap" %}
```url
https://www.leadboxer.com?firstName={vNaam}&lastName={aNaam}&email={email}&companyName={bedrijf}
```
{% endcode %}

