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
<Columns layout="auto">
  <Column>

The **Get OBA Access Code** API is used across different account lifecycle events. Whether you are adding a new shipping account, transitioning a Sandbox account to Production, or linking a new location to an existing account (via UI or API), SAPIENT coordinates with Royal Mail to validate and activate shipping capabilities by calling the **OBA Access Code** API.

  </Column>
  <Column>

> 📘 _Key scenarios covered_
>
> _• Adding a new shipping account_
> _• Changing account type from Sandbox to Production_
> _• Linking a new location to an existing account_
> _• Post-approval activities_

  </Column>
</Columns>

<Accordion title="Adding Royal Mail shipping account" icon="fa-plus">

1. After sending the Royal Mail Add Account request with all mandatory fields populated except the OBA access code, SAPIENT sends a **Get OBA Access Code** Request to Royal Mail.
2. If Royal Mail responds successfully, the shipping account is created in the **Active** status.
3. If Royal Mail returns an error, the account is not created, and SAPIENT returns the [error response](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#possible-oba-error-codes).

> 📘 _Note_
>
> _If the <Glossary>account type</Glossary> is set to **Sandbox** and the OBA access code is not provided, SAPIENT does not send a request to Royal Mail and the account is created successfully without an OBA access code. You can use this account to create test shipments_

</Accordion>

<Accordion title="Changing account type from Sandbox to Production" icon="fa-exchange-alt">

1. If you change the Royal Mail shipping account type from **Sandbox** to **Production**, SAPIENT sends a **Get OBA Access Code** request to Royal Mail.
2. If Royal Mail responds successfully, the account type is updated to **Production**.
3. If Royal Mail responds with an error, the account remains as **Sandbox**, and an [error message](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#possible-oba-error-codes) is returned.

> 🚧 _Important_
>
> _If your shipping account has multiple locations linked to it, then before transitioning to **Production**, keep in mind the following:_
>
> * _SAPIENT sends a separate **OBA Access Code** request for each linked location._
> * _All locations must succeed for the account to be updated to **Production**._
> * _If any location fails, the account remains as Sandbox._
> * _Once you switch from **Sandbox** to **Production**, the system makes a one-time **OBA Access Code** request. If the switch is successful, future changes to the account type will not trigger another OBA call, since the account is already approved and active._

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

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._

To view a step-by-step process on how to add a shipping account with a new shipping location, refer to the following API recipe:

<Recipe slug="create-a-royal-mail-shipping-account-with-a-new-shipping-location" title="Create a shipping account with a new shipping location" />

</Accordion>

<Accordion title="Possible OBA error codes" icon="fa-exclamation-triangle">

<Table align={["center","left","left"]}>
  <thead>
    <tr>
      <th>
        Error Code
      </th>

      <th>
        Error Message
      </th>

      <th>
        Error failure
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        E0004
      </td>

      <td>
        <br />OBA registration failed - Account Number does not exist in OBA
      </td>

      <td>
        AccountNumber
      </td>
    </tr>

    <tr>
      <td>
        E0005
      </td>

      <td>
        OBA registration failed - Account Number does not have an associated Registered Email Address
      </td>

      <td>
        AccountNumber
      </td>
    </tr>

    <tr>
      <td>
        E0006
      </td>

      <td>
        OBA registration failed - Registered Email Address is not linked to the Account Number
      </td>

      <td>
        AccountRegisteredEmail
      </td>
    </tr>

    <tr>
      <td>
        E0007
      </td>

      <td>
        OBA registration failed - Posting Location Number (PLN) does not exist
      </td>

      <td>
        PostingLocationCode
      </td>
    </tr>

    <tr>
      <td>
        E0008
      </td>

      <td>
        OBA registration failed - Registered Billing Postcode does not match
      </td>

      <td>
        RegisteredBillingPostcode
      </td>
    </tr>

    <tr>
      <td>
        E0009
      </td>

      <td>
        OBA registration failed - Shipping Location postcode does not match 
      </td>

      <td>
        Postcode
      </td>
    </tr>

    <tr>
      <td>
        E0011
      </td>

      <td>
        OBA registration failed - Please try again later
      </td>

      <td>
        ObaAccessCodeApi
      </td>
    </tr>

    <tr>
      <td>
        E0012
      </td>

      <td>
        OBA registration failed - Account number is not active (E01) or suspended (E05)
      </td>

      <td>
        AccountNumber
      </td>
    </tr>

    <tr>
      <td>
        E0013
      </td>

      <td>
        OBA registration failed - Posting Location Number (PLN) is not linked to the Account Number 
      </td>

      <td>
        PostingLocationCode
      </td>
    </tr>

    <tr>
      <td>
        E0016
      </td>

      <td>
        OBA registration failed - Matching record already exist in OBA
      </td>

      <td>
        ObaAccessCodeApi
      </td>
    </tr>
  </tbody>
</Table>

</Accordion>

<br />

<Cards columns={1}>
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square">
    Modify an existing Royal Mail shipping account's details.
  </Card>
</Cards>