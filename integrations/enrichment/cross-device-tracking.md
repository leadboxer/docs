# Cross device tracking

### Background

In order to create an unique single profile of a user, every user is assigned an unique user ID (or **uid** technically).&#x20;

This user ID is automatically created by our lead pixel (tracking javascript) that is installed on a website and once generated, we store this uid inside a (first-party) cookie on the users browser.&#x20;

This is useful so that we can check for every next event or action if this user is already know to us, by checking the existence of the cookie and if present, use the uid that is stored inside.

### Cross device tracking

Above approach works very well but can lead to duplicate user entries when users use more then one browser, multiple devices or even delete their cookies.

To minimize this from happening, we offer 2 ways to override the default cookie creation:

1. **uid override**\

2. **email override**

#### 1. uid override

If you know the uid of an existing user, (eg from our API) and you want to make sure their next behavioural action is merged into this existing user, you can 'send' us the uid by adding the **lb\_uid** parameter to a landing page. We will then set or update the cookie to reflect this UID, and thus store all new sessions and event with this user ID.

**URL example**

```
https://www.yourdomain.com?lb_uid=1495157259.1528045459293
```

**Example use case**

You track the (anonymous) visit of a user from Company A, then with some prospecting you figure out who this person is and through email you send them a link that includes the uid from this original visit. If this person then clicks on this link, we will update the previously anonymous user with the details from the second session.

**Possible side affects**

This could lead to multiple users using the same user ID (eg if the url with lb\_uid is shared) and as a result we will store the behaviour of multiple people in one user profile.

**Using your own User ID's**

The lb\_uid parameter also gives you the option to bypass our **uid** generation all together, by providing a customised **uid** through this URL. We will then set the cookie with this uid value. The custom user ID's value should be in "\<number>.\<number>" format.

#### 2. email override

If your already know the email address of the user you want to track, you can include the email address as a parameter in the url of the landing page. We will then lookup if the email is already registered in your data and set or update the cookie to reflect this value.

**URL example**

```
https://www.yourdomain.com?email=jack@leadboxer.com
```

**Example use case**

If you send out a newsletter / campaign or individual email that includes a link to your domain, we will then update existing or create new users and attach that email as a property to the profile of the user.

**Possible side affects**

You expose the email address inside the URL of the landing page. Even though this is not an security risk (as this data is transferred through secure https connections) it does show the user you are actively tracking their behaviour.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on January 23, 2019
