---
description: Formerly known as Spotler or MailPlus
---

# Spotler mail+

### 1. Track Spotler Email opens or reads:

1.  Add a new HTML or code block to the footer of your template

    <figure><img src="../../../.gitbook/assets/Spotler (2).png" alt=""><figcaption></figcaption></figure>
2.  Clcik the HTML/code view and add the tracking code

    <figure><img src="../../../.gitbook/assets/Spotler (3).png" alt=""><figcaption></figcaption></figure>

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR-DATASET-ID&campaign=Spotler-Campaign-[date:en|dd-MM-yyyy|now]&email={email}&firstName={Voornaam}&lastName={Achternaam}&companyName={Bedrijfsnaam}">
```
{% endcode %}

{% hint style="info" %}
Make sure you change YOUR-DATASET-ID in above snippet.

Unfortunatly, Spotler does not have the option to dynamically use the title of the email in the campaign variable, meaning you will need to either use a generic campaign name with a dynamically generated date or manually change this for each email that is send out.
{% endhint %}

### 2. Tracking Spotler clicks

First we recommend you enable the Google Analytics integration, so that UTM tags are added to all the URLs

Secondly, we need to add identification parameters to every URL. This can be accomplished by using the 'Extra parameters' feature. We recommend to add the email and company parameter.

<figure><img src="../../../.gitbook/assets/Spotler (4).png" alt=""><figcaption></figcaption></figure>

Even though it looks like it is enabled for for all emails like this, we found It might be necessary to manually enable this again in the emails/ newsletters themselves.

&#x20;Click on the Analytics button at the top of the email

<figure><img src="../../../.gitbook/assets/Spotler (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Spotler (5).png" alt=""><figcaption></figcaption></figure>

The Extra parameters feature only allows for 2 additional parameters, so if you need more you can still manually add them like this:

{% code overflow="wrap" %}
```url
https://www.leadboxer.com?firstName={vNaam}&lastName={aNaam}&email={email}&companyName={bedrijf}
```
{% endcode %}

