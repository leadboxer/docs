# Constant Contact

Tracking Pixel example

```
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=CAMPAIGNNAME&email=$Subscriber.Email”/>
```

If you want to pass more details you can do so:

```
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=CAMPAIGNNAME&firstName=$Subscriber.FirstName&lastName=$Subscriber.LastName&email=$Subscriber.Email&companyName=$Subscriber.CompanyName"/>
```

That should take care of tracking email opens.&#x20;

As for tracking email clicks and identifying your readers on your site you should similarly append these variables to the links in your emails like this:

```
https://yourdomain.com/?firstName=$Subscriber.FirstName&lastName=$Subscriber.LastName&email=$Subscriber.Email&companyName=$Subscriber.CompanyName
```

You can add custom properties as well if you have these stored in your database. See details here:

Please let me know if this works&#x20;
