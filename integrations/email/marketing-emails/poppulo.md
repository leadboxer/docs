# Poppulo

1. To track mail open/reads:
   1.  edit one of the elements in the footer

       <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c5d55b72c7d3a66e32e2e58/file-fIKLw7pVzD.png" alt=""><figcaption></figcaption></figure>
   2.  switch to the HTML/code view&#x20;

       <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c5d56012c7d3a66e32e2e5b/file-YbPKFfYAVs.png" alt=""><figcaption></figcaption></figure>
   3.  add the tracking code**Use this code:** (Note: Don't forget to Change datasetId and campaign name)

       ```
       <img src="https://track.leadboxer.com/log?datasetId=YOUR_DATASET_ID&campaign=EXAMPLE-Campaign&email=[@subscriberField 'emailAddress.email'/]"/>
       	
       ```

       <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c5d562c2c7d3a66e32e2e60/file-XdnVMD63e5.png" alt=""><figcaption></figcaption></figure>
2.  Tracking clicks&#x20;

    Modify your links and add the parameters like this:

    ```
    https://www.MYSITE.COM?firstName=${subscriber.field('name.firstName')!''}&lastName=${subscriber.field('name.surname')!''}&email=${subscriber.field('emailAddress.email')!''}&companyName=${subscriber.field('company')!''}
    ```

    NOTE: be sure to replace MYSITE.COM with your website-domain landing page

    Its best practice to construct the links in a simple text editor before you paste them into the email:&#x20;

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c5d57b82c7d3a66e32e2e72/file-jEcraiKKHo.png" alt=""><figcaption></figcaption></figure>
