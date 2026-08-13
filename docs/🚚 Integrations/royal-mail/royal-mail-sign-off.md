---
title: Royal Mail OBA account validation and sign-off
excerpt: >-
  Sign-off is a process used by the carrier that all necessary steps have been
  completed before using it for creating the shipments.
deprecated: false
hidden: false
icon: far fa-clipboard-check
metadata:
  robots: index
---
The **Get OBA Access Code** API is used across different account lifecycle events. Whether you are adding a new shipping account, transitioning a Sandbox account to Production, or linking a new location to an existing account (via UI or API), SAPIENT coordinates with Royal Mail to validate and activate shipping capabilities by calling the **OBA Access Code** API.

This section outlines the sign-off process for each scenario, highlights key API interactions and error handling to help customers navigate setup and updates with confidence.

<Accordion title="Adding Royal Mail shipping account" icon="fa-plus">
  1. After sending the Royal Mail Add Account request with all mandatory fields populated except the OBA access code, SAPIENT sends a **Get OBA Access Code** Request to Royal Mail.
  2. If Royal Mail responds successfully, the shipping account is created in the **Active** status.
  3. If Royal Mail returns an error, the account is not created, and SAPIENT returns the [error response](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#possible-oba-error-codes).

  <Callout icon="📘" theme="info">
    ### _Note_

    _If the <Glossary>account type</Glossary> is set to&#x20;_**_Sandbox_**_&#x20;and the OBA access code is not provided, SAPIENT does not send a request to Royal Mail and the account is created successfully without an OBA access code. You can use this account to create test shipments_
  </Callout>
</Accordion>

<Accordion title="Changing account type from Sandbox to Production" icon="fa-exchange-alt">
  1. If you change the Royal Mail shipping account type from **Sandbox** to **Production**, SAPIENT sends a **Get OBA Access Code** request to Royal Mail.
  2. If Royal Mail responds successfully, the account type is updated to **Production**.
  3. If Royal Mail responds with an error, the account remains as **Sandbox**, and an [error message](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#possible-oba-error-codes) is returned.

  <Callout icon="🚧" theme="warn">
    ### _Important_

    _If your shipping account has multiple locations linked to it, then before transitioning to_**_Production_**_, keep in mind the following:_

    - _SAPIENT sends a separate_**_OBA Access Code_**_&#x20;request for each linked location._
    - _All locations must succeed for the account to be updated to_**_Production_**_._
    - _If any location fails, the account remains as Sandbox._
    - _Once you switch from_**_Sandbox_**_&#x20;to&#x20;_**_Production_**_, the system makes a one-time&#x20;_**_OBA Access Code_**_&#x20;request. If the switch is successful, future changes to the account type will not trigger another OBA call, since the account is already approved and active._
  </Callout>
</Accordion>

<Accordion title="Linking a new location to an existing shipping account" icon="fa-link">
  1. When you send the Link Location request, SAPIENT sends the **Get OBA Access Code** request to Royal Mail.
  2. If Royal Mail responds successfully, the location is linked to the shipping account and a successful response is returned.
  3. If Royal Mail responds with an error, the location is not linked, and an [error message](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#possible-oba-error-codes) is returned.
</Accordion>

<Accordion title="Post-approval activities" icon="fa-clipboard-check">
  After your shipping account has been approved by Royal Mail,  the status of your shipping account is changed to **'Enabled'**. Optionally, as part of the post-approval activities, you may perform the following tasks:

  1. You can check the account status by viewing the shipping account or via the [Get Account](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-rm-shippingaccountid) API.
  2. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.

  <Callout icon="📘" theme="info">
    ### _Note_

    _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._
  </Callout>

  To view a step-by-step process on how to add a shipping account with a new shipping location, refer to the following API recipe:

  <Recipe slug="create-a-royal-mail-shipping-account-with-a-new-shipping-location" title="Create a shipping account with a new shipping location" />
</Accordion>

<Accordion title="Possible OBA error codes" icon="fa-exclamation-triangle">
  | Error Code | Error Message                                                                                 | Error failure             |
  | :--------: | :-------------------------------------------------------------------------------------------- | :------------------------ |
  |    E0004   | <br />OBA registration failed - Account Number does not exist in OBA                          | AccountNumber             |
  |    E0005   | OBA registration failed - Account Number does not have an associated Registered Email Address | AccountNumber             |
  |    E0006   | OBA registration failed - Registered Email Address is not linked to the Account Number        | AccountRegisteredEmail    |
  |    E0007   | OBA registration failed - Posting Location Number (PLN) does not exist                        | PostingLocationCode       |
  |    E0008   | OBA registration failed - Registered Billing Postcode does not match                          | RegisteredBillingPostcode |
  |    E0009   | OBA registration failed - Shipping Location postcode does not match                           | Postcode                  |
  |    E0011   | OBA registration failed - Please try again later                                              | ObaAccessCodeApi          |
  |    E0012   | OBA registration failed - Account number is not active (E01) or suspended (E05)               | AccountNumber             |
  |    E0013   | OBA registration failed - Posting Location Number (PLN) is not linked to the Account Number   | PostingLocationCode       |
  |    E0016   | OBA registration failed - Matching record already exist in OBA                                | ObaAccessCodeApi          |
</Accordion>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square" target="_blank">
    Modify an existing Royal Mail shipping account's details.
  </Card>
</Cards>
