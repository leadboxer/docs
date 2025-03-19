# 1. Setup Tracking Pixel

### Introduction

One of the unique features of LeadBoxer is the option to track the behaviour of all the marketing emails you send out. To accomplish this, we provide a generic email tracking pixel for all accounts. You can use this tracking pixel free of charge. We use the same generic tracking pixel in all our tutorials and documentation.&#x20;

## Improve Tracking with a Custom Tracking Domain

Enhancing your email marketing campaigns with a custom tracking domain not only improves brand consistency but also ensures accurate tracking as some email clients and email providers block tracking pixels from 3rd party domains. Follow this guide to set up your custom tracking domain for using Leadboxer.

### Step 1: Configure Your DNS

To begin, you'll need to create a CNAME record in your DNS settings

* **Name:** Choose a subdomain like `logo.yourdomain.com`
* **Value:** Point this to `pixel.leadboxer.com`

Save your changes. Keep in mind that DNS propagation can take up to 24 hours.

### Step 2: Update Leadboxer Settings

Next, log into your Leadboxer account and add your tracking domain:

<figure><img src="../../../.gitbook/assets/Cursor_and_LeadBoxer_App (2).png" alt=""><figcaption></figcaption></figure>



1. Navigate to [Custom Tracking Domain](https://app.leadboxer.com/integrations-connectors/email/custom-tracking-domain)
2. Add your new tracking domain and verify it
3. Once verified, click save and wait 60 seconds
4. Ensure the status shows "Verified" after DNS propagation

### Step 3: Implement the Tracking Domain

1. Replace the default tracking pixel URL with your custom domain\
   For example:\
   track.leadboxer.com --> logo.mydomain.com
2. Ensure all outgoing emails use the new tracking domain for consistency and accuracy

### Benefits

* **Branding:** Maintain a consistent brand presence
* **Improved Deliverability:** Reduce spam risks with matching domains
* **Enhanced Analytics:** Achieve more accurate tracking data
