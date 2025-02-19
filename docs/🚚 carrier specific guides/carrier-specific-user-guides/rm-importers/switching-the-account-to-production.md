---
title: Switch account to production
excerpt: >-
  The switching of the account to the **Production** environment occurs after
  thorough testing is completed in the **Sandbox** environment, ensuring that
  all functionalities work as intended, bugs have been fixed, and performance is
  optimised.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Following the [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) run and approval, and successful UAT (user acceptance test), your account is switched from **Sandbox** to **Production**. 

To set up the live <<glossary:shipping account>>, perform the following steps.

1. Add a [shipping account](https://docs.intersoftsapient.net/docs/add-a-shipping-account), ensuring that the <<glossary:account type>> is set to **Production**, and it is prepopulated with the correct Royal Mail account details, Royal Mail Account Number, Posting Location and Account Registered Email (email address used to access your <<glossary:Online Business Account>> (OBA) to view billing and reporting). For more information on how to fill in the fields, refer to the [Set up Royal Mail shipping account.](https://docs.intersoftsapient.net/docs/shipping-account-requirements) section.
2. After adding/setting up the shipping account, an automatic request is be sent to the OBA team. It may take 2-5 working days for them to review it and either accept it or reject it (depending if the RM account details provided are correct). 
3. If the OBA request is accepted, the **Account Status** is changed from **Disabled** to **Enabled**. Otherwise, it remains disabled and you need to go back and fill in the correct Royal Mail account details and send the request again. 

> 💡 _Tip_
> 
> _The shipping account you set up previously stay as the **Sandbox** account type and you can continue using it for testing purposes._

4. If you are a freight 2 post customer, ensure that [international arrival containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers) is set up with valid details provided to you by Intersoft Onboarding team. 
5. After, you you can proceed with the **label sign off** required by Royal Mail. The sign off depends on what type of Royal Mail you are:

- **Royal Mail importers using Commercial Clearance route and Tracked High Volume customers**: involves physical label sign off—where you are requested to create couple of labels, manifest them and ship them to Royal Mail.
- **Royal Mail importers using Freight 2 Post route**: involves CDS checks as well as physical label sign off. For  
  CDS checks, you are requested to create a couple of <<glossary:labels>>, <<glossary:manifest>> them and share with us the <<glossary:PDF>>s, so they can be checked in first as part of the account set up process. 

The full details on this are shared with you closer to the date.

6. Once the labels are signed off and the go-live action is agreed with Royal Mail,  you can start shipping via Intersoft SAPIENT.

## See also

If you are interested in creating a tracking account for the newly added shipping account, refer to the following sections on how to set up our <<glossary:tracking webhook>> solution:  

- [Tracking webhook](https://docs.intersoftsapient.net/docs/tracking-webhook-1): set up the webhook connection, create tracking account, and much more.
- [Response examples](https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample): view response example of the tracking webhook push notification payload, as sent to a customer's webhook when tracking information is received from a carrier.  
- [Royal Mail tracking account setup](https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup): set up Royal Mail tracking account.

> 📘 _Note_
> 
> _To enable the **Tracking Webhook** solution, please contact our [Intersoft Onboarding](mailto:onboarding@intersoft.co.uk) team._