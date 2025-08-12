---
title: Royal Mail sign-off
excerpt: >-
  Sign-off is a process used by the carrier that all necessary steps have been
  completed before using it for creating the shipments.
deprecated: false
hidden: false
icon: far fa-clipboard-check
metadata:
  robots: index
---
Once you have created the Royal Mail <Glossary>shipping account</Glossary>, the account needs to be approved before you start using it to ship with Royal Mail.

To get your shipping account approved, consider the following:

1. If the <Glossary>account type</Glossary> you have created is **Production**, you will receive a confirmation email.
2. Initially, the account status is set to **'Disabled'** until the account has been approved by the Royal Mail <Glossary>Online Business Account</Glossary> (OBA) team. This can typically take 2-5 working days.
3. Once the account has been approved, the status of your shipping account is changed to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-rm-shippingaccountid) API.
4. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.
5. If the account cannot be approved, we will contact you and advise accordingly.

> 📘 *Note*
>
> *Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section.*

To view a step-by-step process on how to add a shipping account with a new shipping location, refer to the following API recipe:

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)