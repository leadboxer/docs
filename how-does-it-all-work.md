---
description: >-
  How do LeadBoxer and its components actually work.  What can you do with the
  platform? What do we actually capture and how?
---

# How does it all work?

This is not an easy question to answer 1-2-3, as LeadBoxer does many things. 😉 So here are some of the basic concepts:

* [Identification](how-does-it-all-work.md#identification)
  * [IP address](how-does-it-all-work.md#ip-address)
  * [Forms](how-does-it-all-work.md#forms)
  * [Integrations](how-does-it-all-work.md#integrations)
* [Behavioural Tracking](how-does-it-all-work.md#behavioural-tracking)
  * [Website](how-does-it-all-work.md#website)
  * [Email](how-does-it-all-work.md#email)
  * [Other](how-does-it-all-work.md#other)
* [Enrichment](how-does-it-all-work.md#enrichment)
  * [Firmographic](how-does-it-all-work.md#firmographic-enrichment)
  * [First party](how-does-it-all-work.md#first-party-data)
* [From Leads to Opportunities](how-does-it-all-work.md#from-leads-to-opportunities)
  * [Qualification](how-does-it-all-work.md#qualification)
  * [Management](how-does-it-all-work.md#lead-management)

## Identification

At LeadBoxer, we use multiple techniques to identify both the Organizations and Individuals that interact with our clients websites, emails, marketing tools, chatbots, portals, apps or any other digital platform they are using. Here is a description of the most commonly used touchpoints:&#x20;

### IP address

One of the oldest and best-known techniques to identify website visitors is by analyzing the IP addresses associated with their internet connection (also known as ip lookup). This can be used to identify companies and organizations that visit a website.&#x20;

Every device that connects to the internet is assigned an IP (Internet Protocol) address; a unique numerical identifier that allows devices to communicate with each other over the internet. IP addresses can be used to determine the approximate geographic location of a device and can also be associated with specific organizations.

To identify the companies behind IP addresses, we use a combination of advanced techniques to map IP addresses to specific companies or organizations. We've been building our proprietary identification technology for close to twenty years.

It's important to note that while IP-based company identification can be a useful tool for businesses and marketers, it is not always accurate. IP addresses can be shared, sold, hired or masked, and not all organizations have a unique IP address associated with their internet traffic. Additionally, some businesses may use virtual private networks (VPNs) or proxy servers to obfuscate their IP address and maintain their privacy.&#x20;

At LeadBoxer, we are constantly updating our technology and databases and keep track of changes and (technical) updates to make sure we always provide you with the 'most likely' outcome of who is actually behind an IP address at that moment.&#x20;

### Forms

Another well-known technique is [Form tracking](integrations/website/manual-form-tracking.md): to capture or track what people fill out on a web form and attach or connect that to the user who is visiting your website. This can include their email, name, company, etc.&#x20;

You can do this for any form, for example a newsletter signup, a lead-magnet or white-paper download, etc. but also chatbots, 'wizards', price calculators, etc.

Once the person or organization is identified, this will stored and for retroactive (previous) and future identification when activity takes place. Subsequent sessions will be connected to this person and organization (if relevant).

### Integrations

By using any of the [integrations we support](how-does-it-all-work.md#integrations) (or by building your own) you can enable LeadBoxer to use the first-party data available in your marketing and sales tools, and, so-to-speak 'connect-the-dots': identify these contacts and accounts in LeadBoxer. The result will be a central Lead Generation hub: Lead Identification, Lead Qualification, and Lead Management.

## Behavioural Tracking

LeadBoxer makes (among other techniques) use of website tracking pixels, also known as a tracking script, tag, code or a web beacon. [Our tracking script](integrations/website/lead-tracking-pixel.md) is a small, highly optimized, load-balanced snippet of javascript that -at its core- fires a small, invisible image file with a width and height of 1x1 pixel (hence the name tracking pixel) that is then embedded into a website or an email. The purpose of the tracking pixel is to track user behavior and collect data about how users interact with website or email.

### Website

When a user visits a website that contains our tracking pixel, their web browser requests the image file from our servers that hosts the pixel. This request sends information such as the user's IP address, browser type, and referring URL to our servers. The servers can then use this information to track the user's activity on the website, such as the pages they visit, the links they click, and the time they spend on each page.

Here's how it works in more detail:

1. The LeadBoxer tracking JavaScript code is added to a website's HTML code.
2. When a visitor loads a page on the website, the LeadBoxer JavaScript code creates an Image object, sets the source of the image to the URL of our tracking server, and appends the image to the document.
3. The browser then makes a request to our tracking server to load the image. This request includes the URL and title of the page in the referrer header.
4. Our tracking server receives the request and logs the URL and title of the page along with other data such as the user's IP address and browser information, utm tags, etc.
5. The tracking servers pass on this data to our processing servers, which in return try to **Identify** the organization and/or person and **enrich** the data before it gets stored in our secure and private cloud.&#x20;

**Cookies**\
Perhaps needless to say; our tracking javascript does a lot more just load the tracking pixel image. We also set and read first-party browser cookies, so we can identify the browser when there are multiple requests or pageviews, and string these together into a session and recognise the browser upon return. We do not store any personally identifiable information (PII) in our first-party cookies. Additional details can be found on the [LeadBoxer Cookies](extras/leadboxer-cookies.md) page.

### Email

Similar to website tracking, the core technique for email tracking is adding a 1x1 transparent pixel image into the body of an email, which tells the LeadBoxer servers an email is opened or read.

As very few email clients support javascript, there is less data that can be captured, meaning the signals we receive are most useful when translated into basic behavioural events.&#x20;

As part of a 'customer journey,' however, they can be quite powerful. Think about 'individual buyer intent' or 'buy signals' here.&#x20;

Another option with email tracking is to track the clicks inside an email to your website, which also can trigger an Identification. In other words when and if that person visits your website after receiving an email, even months later.

### Additional behavioral data types&#x20;

We also support other kinds of behavioral data, for example data from an ERP, CRM, telemarketing, shopping systems, registers, etc. This data can be transferred to LeadBoxer using our API or even via file transfer. This enables our customers to connect even more dots and create complete lead, opportunity or customer 360 views.



## Enrichment

### Firmographic&#x20;

This is the process of enhancing business data by adding additional firmographic attributes to existing records. Firmographic data refers to the characteristics that define a business entity, such as its industry, size, location, and revenue. This additional information may come from a variety of sources, such as public records, business directories, or third-party data providers.

The purpose of firmographic enrichment is to create a more complete and accurate picture of a company's profile. By enriching business data with additional firmographic attributes, our clients can gain valuable insights into their leads, customers, prospects, etc.&#x20;

Some common firmographic attributes that may be added through enrichment include:

* Industry classification
* Company size (number of employees, revenue)
* Geographic location
* Ownership type (public or private)
* Years in business
* Contact information (phone, email, address)
* Technograpic data (what technologies are in use)
* Social data (LinkedIn, Facebook, Twitter, etc)

Firmographic enrichment is very useful for businesses that rely on data-driven decision-making and sales and marketing teams. By having more complete and accurate information about their target audience, these teams can create more effective marketing campaigns, improve lead generation efforts, and ultimately drive revenue growth.

### First Party data&#x20;

Similar to using marketing and sales tools to identify more leads and opportunities, you can also enrich the accounts and Leads in LeadBoxer with data that you already have. You can then use this data to better filter, score and segment the different audiences you might have.&#x20;

A good example is to be able to 'tag' or 'label' your existing client base to either filter them out of your Lead Generation efforts or to filter these in to monitor for upsell opportunities.

Obviously there are many other use-cases that drive value by 'simply' connecting the dots and making sure they are shown to the right person at the right time.

## From Leads to Opportunities

Once we have Identified the companies, organizations and contacts that interact with our clients content, and we also know which content they are interested in, we define the Segments or Target Audiences that our clients are interested in. For example, we can filter out job-seekers, existing clients, but include organizations that have the right size, industry, location, and also have downloaded a specific whte-paper, etc.

We get from Leads to Opportunities using **Lead Qualification** and **Lead Management**.

### Qualification

In General, Lead qualification helps companies prioritize their sales efforts and focus on the leads that are most likely to convert into customers. This, in turn, helps companies save time and resources by avoiding wasting time on leads that are unlikely to convert.

At LeadBoxer, Lead qualification is the process of evaluating the readiness and likelihood of a potential customer to become a paying customer. The process involves collecting and analyzing data about a lead, such as their interests, company profile, budget, timeline, authority, and need, to determine if they are a good fit for a company's product or service.&#x20;

During lead qualification, the lead is assessed against predefined criteria using [Filters](fundamentals/elements/filters.md) and [Segments](fundamentals/elements/segments.md) to determine if they meet the minimum requirements to move forward in a lead qualification process or workflow or Lead Management solution.

### Lead Management

Lead management is basically the process of capturing, tracking, and nurturing potential customers or leads as they progress through the marketing or pre-sales funnel. It involves managing interactions with leads at each stage of the buyer's journey, from initial awareness to sales qualified lead (SQL) and even beyond.

The goal of lead management is to maximize the number of qualified leads that can be passed on to sales, while minimizing the time and resources spent on unqualified leads.&#x20;

In LeadBoxer this can be achieved using the [LeadBoard](fundamentals/tasks.md), where our clients can visually research and move leads manually or automatically through their workflow or qualification process until they become actual opportunities.

A typical example is that once a Lead fits the final criteria, they are deemed 'sales qualified' and handed over to the sales team for further engagement.

Advanced use-cases can be implemented by creating multiple LeadBoards, for example one for each region, sales team, product or service category, and even linking multiple boards together to create a workflow across multiple teams.

Effective lead management can help companies improve their sales performance, optimize their marketing efforts, and increase their overall revenue.



To learn more about LeadBoxer, you are most welcome to [schedule a call](https://www.leadboxer.com/start) with us.&#x20;

\
