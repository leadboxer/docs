---
description: Here you can find the instructions to Enable SSO for LeadBoxer
---

# Single Sign On (SSO)

### Prerequisites <a href="#h_cd7bfcb583" id="h_cd7bfcb583"></a>

1. A LeadBoxer Enterprise account
2.  A valid SSO service.&#x20;

    At the moment we support Microsoft Entra ID (previously Azure Active Directory)\
    contact us if you need us to support other SSO providers
3. All users that you want to provide LeadBoxer access through SSO also need to be present in LeadBoxer as users.

## Microsoft Entra ID setup  <a href="#h_2fe40bd98a" id="h_2fe40bd98a"></a>

1. Log into your Azure Portal
2. Go to Enterprise Applications

<div align="left">

<figure><img src="../../.gitbook/assets/All_services_-_Microsoft_Azure (1).png" alt=""><figcaption></figcaption></figure>

</div>

3. Create a new Application

<figure><img src="../../.gitbook/assets/Enterprise_applications_-_Microsoft_Azure.png" alt=""><figcaption></figcaption></figure>

4. Provide a name, eg: LeadBoxer SSO\
   and set "Integrate any other application you don't find in the gallery (Non-gallery)"

<figure><img src="../../.gitbook/assets/Create_your_own_application_-_Microsoft_Azure.png" alt=""><figcaption></figcaption></figure>

5. Once the application is created,\
   Proceed to the "Single sign-on" option.\
   Select "SAML" as the authentication method.

<figure><img src="../../.gitbook/assets/LeadBoxer_SSO_-_Microsoft_Azure.png" alt=""><figcaption></figcaption></figure>

6.  On the next screen, edit the Basic SAML configuration, and set the following URLs:

    \
    Identifier (Entity ID):

    `https://lbapiv2/saml2/service-provider-metadata/adfs`

    \
    Reply URL (Assertion Consumer Service URL):

    `https://lb1.leadboxer.com/login/saml2/sso/adfs`\


    <figure><img src="../../.gitbook/assets/Basic_SAML_Configuration_-_Microsoft_Azure (1).png" alt=""><figcaption></figcaption></figure>
7.  The last step is to copy and share with us the "App Federation Metadata Url" located under the "SAML Certificates" section.

    <figure><img src="../../.gitbook/assets/LeadBoxer_SSO_-_Microsoft_Azure (1).png" alt=""><figcaption></figcaption></figure>
8. Once we have received the App Federation Metadata Url from you, we will add it to our settings and confirm.&#x20;

## Login

Once confirmed  your users can log into LeadBoxer using their SSO Account.

<figure><img src="../../.gitbook/assets/LeadBoxer_App (24).png" alt=""><figcaption></figcaption></figure>

## Microsoft Entra ID login <a href="#h_2fe40bd98a" id="h_2fe40bd98a"></a>

1.  Use the Login with Microsoft button

    <figure><img src="../../.gitbook/assets/LeadBoxer_App (25).png" alt=""><figcaption></figcaption></figure>
2. Login and /or authenticate with your Microsoft account
3. Once authenticated you will get redirected to the application

{% hint style="warning" %}
Any user that you want to provide LeadBoxer access through SSO also need to be present in LeadBoxer as a user.
{% endhint %}

