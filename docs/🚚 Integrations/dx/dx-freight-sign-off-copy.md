---
title: DX Express sign-off
excerpt: >-
  Sign-off is a process used by the carrier that all necessary steps have been
  completed before using it for the creation of shipments.
deprecated: false
hidden: false
icon: far fa-clipboard-check
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Once you have created the DX Express <Glossary>shipping account</Glossary>, make sure you have the correct information before you start using it to ship with DX Express.

> 💡 *Tip*
>
> *The DX Express integration is pre-approved, but you must have the required information beforehand to ship with DX Express.*

In order to ship with DX Express, consider the following:  

1. The API credentials have been [created and obtained](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials).
2. Set up the shipping account with the <Glossary>account type</Glossary> set to **Production**.
3. Once the account has been created with the correct information, the status of your shipping account is set to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://api.test.intersoftsapient.net/docs/v4-DX/api/index.html#tag/Shipping-Accounts/paths/~1v4~1shippingAccounts~1DX~1%7BshippingAccountId%7D/get) API.
4. Although, the Intersoft DX Express integration is approved by the <Glossary>carrier</Glossary>, it is recommended to create a few test <Glossary>labels</Glossary> with services you will be using and share the labels with the carrier for review to avoid any discrepancies.
5. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.