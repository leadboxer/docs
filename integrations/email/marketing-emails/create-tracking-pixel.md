# 1. Create Tracking Pixel

### Introduction

Enhancing your email marketing campaigns with a custom tracking domain not only improves brand consistency but also ensures accurate tracking. Follow this guide to set up your custom tracking domain using Leadboxer.

### Step 1: Configure Your DNS

To begin, you'll need to create a CNAME record in your DNS settings:

* **Name:** Choose a subdomain like `logo.yourdomain.com`
* **Value:** Point this to `pixel.leadboxer.com`

Save your changes. Keep in mind that DNS propagation can take up to 24 hours.

### Step 2: Update Leadboxer Settings

Next, log into your Leadboxer account and add your tracking domain:

1. Navigate to [Custom Tracking Domain](https://app.leadboxer.com/integrations-connectors/email/custom-tracking-domain)
2. Add your new tracking domain and verify it.
3. Once verified, click save and wait 60 seconds.
4. Ensure the status shows "Verified" after DNS propagation.

### Step 3: Implement the Tracking Domain

1. Replace default tracking URLs with your custom domain.
2. Ensure all outgoing emails use the new tracking URL for consistency and accuracy.

### Benefits

* **Branding:** Maintain a consistent brand presence.
* **Improved Deliverability:** Reduce spam risks with matching domains.
* **Enhanced Analytics:** Achieve more accurate tracking data.
