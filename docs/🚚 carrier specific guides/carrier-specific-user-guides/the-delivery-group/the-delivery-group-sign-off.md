---
title: The Delivery Group sign-off
excerpt: >-
  Sign-off is a process used by the carrier that all necessary steps have been
  completed before using it for creating the shipments.
deprecated: false
hidden: false
metadata:
  robots: index
---
Once you have [created](https://docs.intersoftsapient.net/docs/the-delivery-group-account-set-up#/) the Delivery Group (TDG) <Glossary>shipping account</Glossary>, make sure you have the correct information before you start using it to ship with The Delivery Group.

> 💡 *Tip*
>
> *The Delivery Group integration is pre-approved, but you must have the required information beforehand to ship with this carrier.*

In order to ship with The Delivery Group, consider the following:

1. The **Delivery Group Username**and **Delivery Group Password** have been provided to you by the TDG sales team.
2. Set up the shipping account with the <Glossary>account type</Glossary> set to **Sandbox**.
3. After creating the account with the correct information, the status of your shipping account is set to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://api.test.intersoftsapient.net/docs/v4-DX/api/index.html#tag/Shipping-Accounts/paths/~1v4~1shippingAccounts~1DX~1%7BshippingAccountId%7D/get) API.
4. Once everything is set up, you must create a few test labels with services you will be using and share the <Glossary>labels</Glossary> with the TDG onboarding manager.
5. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.
6. After the TDG sign-off, a confirmation will be sent to you agreeing to go live.
7. Now, you can set your account type as **Production** and start shipping with it.