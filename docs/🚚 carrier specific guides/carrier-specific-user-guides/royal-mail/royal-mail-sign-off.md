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
To ensure a seamless integration between SAPIENT and Royal Mail’s shipping services, it is essential to understand how the **Get OBA Access Code** API is used across different account lifecycle events. Whether you are dding a new shipping account, transitioning a Sandbox account to Production, or linking a new location to an existing account either via UI or API, SAPIENT coordinates with Royal Mail to validate and activate shipping capabilities by calling its **OBA Access Code** API.

This section outlines the sign-off process for each scenario, highlights key API interactions and error handling to help customers navigate setup and updates with confidence.

## Adding Royal Mail shipping account

1. After sending the Royal Mail Add Account request with all mandatory fields populated except the OBA access code, SAPIENT sends a **Get OBA Access Code** Request to Royal Mail.
2. If Royal Mail responds successfully, the shipping account is created in the **Active** status.
3. If Royal Mail returns an error, the account is not created, and SAPIENT returns the error response.

> 📘 _Note_
>
> _If the <Glossary>account type</Glossary> is set to **Sandbox** and the OBA access code is not provided, SAPIENT does not send a request to Royal Mail and the account is created successfully without an OBA access code. You can use this account to create test shipments_

## Changing account type from Sandbox to Production

1. If you change the Royal Mail shipping account type from **Sandbox** to **Production**, SAPIENT sends a **Get OBA Access Code** request to Royal Mail.
2. If Royal Mail responds successfully, the account type is updated to **Production**.
3. If Royal Mail responds with an error, the account remains as **Sandbox**, and an error message is returned.

> 🚧 _Important_
>
> _If your shipping account has multiple locations linked to it, then before transitioning to **Production**, keep in mind the following:_
>
> * _SAPIENT sends a separate **OBA Access Code** request for each linked location._
> * _All locations must succeed for the account to be updated to **Production**._
> * _If any location fails, the account remains as Sandbox._
> * _Once you switch from **Sandbox** to **Production**, the system makes a one-time **OBA Access Code** request. If the switch is successful, future changes to the account type will not trigger another OBA call, since the account is already approved and active._

## Linking a new location to an existing shipping account

1. When you send the Link Location request, SAPIENT sends the **Get OBA Access Code** request to Royal Mail.
2. If Royal Mail responds successfully, the location is linked to the shipping account and a successful response is returned.
3. If Royal Mail responds with an error, the location is not linked, and an error message is returned.

## Post-approval activities

After your shipping account has been approved by Royal Mail,  the status of your shipping account is changed to **'Enabled'**. Optionally, as part of the post-approval activities, you may perform the following tasks:

1. You can check the account status by viewing the shipping account or via the [Get Account](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-rm-shippingaccountid) API.
2. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._

To view a step-by-step process on how to add a shipping account with a new shipping location, refer to the following API recipe:

<Recipe slug="create-a-royal-mail-shipping-account-with-a-new-shipping-location" title="Create a shipping account with a new shipping location" />

## Possible OBA error codes

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
        Reason 
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        E0004
      </td>

      <td>
        <br /><br />
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0005
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0006
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0007
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0008
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0009
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0011
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0012
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0013
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        E0016
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

<br />

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)
