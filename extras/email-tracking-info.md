# Email tracking info

## Google Image Proxy for Gmail

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

## Disable or Block email tracking?

We received this related set of questions on the subject(s) of

1. How email tracking works - images, pixels, and downloads
2. How recipients can block or disable tracking and
3. How to can I minimise the risk of having people block my email tracking

Here are the QUESTIONS we received:&#x20;

1. How is the e-mail and document tracking technically performed? Do you attach an image to the e-mail body and by image download track the e-mail, or do you attach a pixel instead? If the second option is the case, can you please indicate what happens next?
2. Is there an option for the recipient to disable or block e-mail tracking? For example, in case of attaching an image to the e-mail, the e-mail client can automatically block image download or the recipient can choose not to download the image, which prevents e-mail tracking. Can you please indicate what is done in case of your product?&#x20;
3. What options does a recipient have to disable e-mail and document tracking? How are the risks of blocking the e-mail and document tracking mitigated?

ANSWERS:

1.  We use a (tracking) pixel which we call a "lead pixel". The result is the same, as an image for example. There is no technical difference between tracking an image or using a pixel. The one difference is that the pixel is not visible (as opposed to an image).

    Think of a pixel as an invisible image.
2. There is no way to track an email (either way, pixel, image, or download) if the recipient does not accept the image(s), or initiate a download. In other words, the outcome is based on the settings or preference(s) of the end-user.\

3. How can i minimise the risk of having people block my tracking? This is a very interesting question. The answer is to make the email informative, (valuable), and put useful images (labeled) in it. In our experience, people will accept tracking if there are useful images - as seen from the tags behind the images.\
   In other words: name your images descriptively - not \[title].png - but something based on content:\
   "chart of climate change impact - depicting planetary damage" -people would be more likely to load image(s). Result: the tracking pixel will also load.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on August 28, 2019
