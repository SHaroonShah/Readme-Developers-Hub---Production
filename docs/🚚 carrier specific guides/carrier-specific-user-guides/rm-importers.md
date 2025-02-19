---
title: Royal Mail import service
excerpt: >-
  The Royal Mail import service is a logistic solution provided by Royal Mail
  that facilitates the importation of goods into the UK from overseas. It is
  designed to simplify the process of receiving international parcels and
  packages, ensuring that they are delivered efficiently and securely to the
  customers.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you wish to use the Royal Mail import services, you can integrate with Intersoft SAPIENT and start your seamless importing journey.  

> 🚧 _Important_
> 
> _This section is only applicable if you are a Royal Mail customer who is importing goods into the UK. Before initiating the integration, make sure you have an agreement with Royal Mail to use this service._

To integrate with the Royal Mail import services via SAPIENT, follow the instructions as explained in the following procedure.

1. At first, ensure to activate your account on SAPIENT. Upon activation, a confirmation email is sent to you from [onboarding@intersoftsapient.net](mailto:noreply@intelligentshipper.net). Proceed to activate your account as directed in the email.

2. After, proceed to [creating your API credentials](https://docs.intersoftsapient.net/docs/create-api-credentials).

3. Now, on the SAPIENT Home page, select **Integrations**. On the **Integrations** page that opens, within the **Royal Mail** block, select **LABELS**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d83f58ad7239cbd1faadbb4d1783adbfceaaef163fb864672d6c2600b954e14e-Rm_lables_integration.png",
        "",
        "Selecting Royal Mail labels integration"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting Royal Mail labels integration"
    }
  ]
}
[/block]


4. On the integrations page that opens, in the **LABELS** block, select **ACTIVATE**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/abc4b6de2300fc06a50a56e87560afb0251fd5a13cf521fff5c473cdc4502d51-RM_Labels_activation.png",
        "",
        "Activating Royal Mail labels integration"
      ],
      "align": "center",
      "border": true,
      "caption": "Activating Royal Mail labels integration"
    }
  ]
}
[/block]


5. Once activated, now proceed to adding the  [shipping account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) and [shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) for Royal Mail.  

> 💡 _Tip_
> 
> _For Sandbox (Test) account, you can fill the information with dummy details. For more information on how to set up a Royal Mail <<glossary:shipping account>> , refer to the [Setup Royal Mail shipping account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) section._

6. If you are a freight 2 post customer, set up [international arrival containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers). For now this can be filled with dummy details. Production details will be provided to you when your account is switched onto production.
7. After, develop all the [API calls required](https://docs.intersoftsapient.net/docs/sandbox-development-api-requirements) considering the specific requirements applicable to you:

- If you are a commercial clearance customer, refer to the [corresponding requirements](https://docs.intersoftsapient.net/docs/commercial-clearance-customers).
- If you are a freight 2 post customer, refer to the [corresponding requirements](https://docs.intersoftsapient.net/docs/freight-2-post-customers).

> 🚧 Please also ensure that you adhere to our [API Rate Limits](https://docs.intersoftsapient.net/docs/api-rate-limiting).

8. Once all the necessary steps have been completed, you are now ready to go live. Before getting you live on board, make sure you complete our [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) and submit it at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

> 📘 _Note_
> 
> _A test pack is a critical step in the implementation process, ensuring a smooth transition to the live environment and minimising disruptions in shipping operations._

9. Once the **Test Pack** is approved, our team will [switch your account to Production](https://docs.intersoftsapient.net/docs/switching-the-account-to-production) and share with you the details on the sign off process required by Royal Mail. 

Please direct any questions or issues with this service to [onboarding@intersoft.co.uk.](mailto:onboarding@intersoft.co.uk.). For INTERSOFT to investigate your issue accordingly, kindly include copies of both the API request and API response.

> 🚧 _Important_
> 
> _While submitting your issues to Intersoft, please do not include your API credentials in the request._

## See also

If you are interested in our tracking solution, refer to the following sections on how to set up our <<glossary:tracking webhook>> solution:  

- [Tracking webhook](https://docs.intersoftsapient.net/docs/tracking-webhook-1): set up the webhook connection, create tracking account, and much more.
- [Response examples](https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample): view response example of the tracking webhook push notification payload, as sent to a customer's webhook when tracking information is received from a carrier.  
- [Royal Mail tracking account setup](https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup): set up Royal Mail <<glossary:tracking account>> .

> 📘 _Note_
> 
> _To enable the **Tracking Webhook** solution, please contact our [Intersoft Onboarding](mailto:onboarding@intersoft.co.uk.) team._