# Google Image Proxy for Gmail

#### Introduction

Starting in 2013, Google introduced a feature for its gmail customers to preload and proxy-load the images that are present in (html) emails. This allows them to provide a better and faster experience when users make use of the web-based email client (at [https://mail.google.com](https://mail.google.com/)) to read their messages.&#x20;

By default, our tracking pixels are not cached, so we can track if emails are actually opened and read.

#### Downside

This pre-loading or proxying of these images does has one main downside: It proxies the images loading from a google owned server, and by doing so it is masking the IP-address and user-agent of the web-browser that is actually requesting the email tracking image. Meaning that we cannot use these values to identify or locate based on IP address or tell you the device they are using to read these emails.

Affected email clients:

* gmail web-app ([https://mail.google.com](https://mail.google.com/))
* gmail app (iOS/android)
* Inbox app (iOS/android)

#### How to improve

For this and many other reasons its always good practice focus your email content (whether its a marketing campaign or individual email) to get them to click on any link in your email that leads them to your site. (with our tracking pixel installed) Once you get them to click, we will be able to identify and enrich based on the IP and user-agent.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on December 30, 2018
