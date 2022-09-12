# Tracking emails with Mail Merge in Microsoft Word

### Tracking email clicks

Tracking individual email clicks requires an unique URL or hyperlinks for each of your recipients.&#x20;

So you will need to customise the or 'build' the url so it becomes unique and contains the parameters you need.

You can do this either inside outlook or prepare the URL's already in your spreadsheet.

#### option 1, construct the URLs in the spreadsheet

Preparing the URL's in your spreadsheet is easier, but requires a bit of advanced copy/pasting. The URLs need to be formatted in this way:

[https://my-desination.url?utm\_medium=email\&email={email}\&firstName={firstname}\&lastName={lastnane}](https://my-desination.url/?utm\_medium=email\&email={email}\&firstName={firstname}\&lastName={lastnane})

Where all the parameters within the curly brackets { } need to be replaced with actual values and the end result is a custom URL for each of your recipients.

#### Option 2, construct the URL in Outlook

For more details see these articles:

[https://www.vapromag.co.uk/mail-merge-with-personalised-hyperlinks/](https://www.vapromag.co.uk/mail-merge-with-personalised-hyperlinks/)

[https://originaldougal.com/email-mail-merge-office-2010-hyperlinks/](https://originaldougal.com/email-mail-merge-office-2010-hyperlinks/)

### Track email Opens

In order for LeadBoxer to track email opens, you need to add the tracking pixel by including a customised picture source URL in the spreadsheet using the { INCLUDEPICTURE "{ MERGEFIELD Url }" } parameter.

the pixel source URL needs to look like this:

```
https://track.leadboxer.com/log?datasetId={{yourDatasetId}}&campaign={{YourCampaignName}}&email={{emailMergTag}}
```

There are 3 values that need to be modified for each row:&#x20;

1. datasetId = this is the ID for the dataset or website you want to track email activity for&#x20;
2. campaignName = the name for your specific campaign&#x20;
3. email = the email address of the recipient.

For more details please see:\
[https://www.experts-exchange.com/questions/28462841/mail-merge-in-word-to-get-picture-link-as-image.html](https://www.experts-exchange.com/questions/28462841/mail-merge-in-word-to-get-picture-link-as-image.html)
