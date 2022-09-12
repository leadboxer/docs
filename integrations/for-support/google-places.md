# Google Maps Integration

The companies database that LeadBoxer uses for enrichment is large and very accurate. But there are many (smaller) companies out there that are not, and will never, make it into the main databases we use such as Linkedin or any of the other sources we use.

For that reason we support the Google Places API for improved enrichment of smaller local companies.

Meaning that if you add a Google maps API key, we will use the Google API to enrich your leads with the places company details like address, domain, and phone number.

### Generate a new API key

1. Go to the [Google Maps Platform](https://cloud.google.com/maps-platform/)
2. Click ‘Get Started’
3. Check only ‘Places’\
   ![Google Maps Enable APIs](https://yoast.com/app/uploads/sites/5/2018/05/google-maps\_enable-api.png)
4. Click ‘Continue’
5. If you want to use an existing project, please select it from the list. Otherwise, select ‘Create a new project’ and enter a project name like LeadBoxer
6. Click ‘Next’ to continue
7. If you haven’t set up your billing account yet, follow the steps Google gives you to set it up.
8. Click ‘Next’ to enable the APIs for the project
9. Copy the generated API key from the popup, you’ll need this to set your key later.

### View your existing API keys

1. Go to the [Google Maps Platform](https://console.cloud.google.com/home)
2. If the side menu is not visible, click the three-line (hamburger) menu icon
3. Click ‘APIs & Services’ (API icon)
4. Click ‘ Credentials’ (key icon)

If the above steps are not clear enough then please follow the tutorial video from the Google Maps Platform Team below. This video will show you how to generate and restrict API keys.

### Add API key to LeadBoxer

1. Copy the API key you created from the [Google Maps Platform](https://console.cloud.google.com/apis/credentials).
2. Log in to your LeadBoxer account as admin.
3. from the the top right menu (under your name) go to integrations and select Google
4. paste the API key into the field for each site/dataset you want to enrich and enable the checkbox
5. Save, and you are done!

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on November 6, 2020
