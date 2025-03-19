---
title: Add FedEx shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a shipping account with FedEx, and then link it to the relevant <Glossary>shipping location</Glossary>(s).

> 🚧 *Important*
>
> *Before setting up the<Glossary>shipping account</Glossary>, make sure you have the following information:*
>
> * *The 9-digit FedEx carrier account number.*
> * *The exact shipping address that you have provided to FedEx, as this information is validated via the**Address Validation** API. If the address does not match, then a corresponding error message is displayed—and you will not proceed to the**Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form.*

To add a shipping account for FedEx in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/0aa0c2e5571aecb4b468578dd7f4575502f692fed3703818183b78c9a4548a82-Add_shipping_account_FedEx.png" width="500px" />

<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Element
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Carrier\***
      </td>

      <td>
        From the dropdown list, select **FEDEX - FedEx**.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Location\***
      </td>

      <td>
        From the dropdown menu, select the location that you want to assign to the shipping account you are creating.

        *`Note`: Before selecting the shipping location, make sure you have[created one](https://docs.intersoftsapient.net/docs/add-a-shipping-location) beforehand.*
      </td>
    </tr>
  </tbody>
</Table>

4. After specifying the carrier and shipping location, a new **CONNECT YOUR FEDEX ACCOUNT** form appears.  At the **Shipping Account** stage of the form, specify the general details associated to your FedEx account number and then select ![alt text](https://files.readme.io/cc0b1ba97fd42622607551903346520543f58dfb3740f9f55eec3021b0a251d0-Next_button.png).
5. At the **Shipping Address** stage that appears, specify the FedEx shipping address details so that the system can validate and match it with the address registered in the FedEx systems. After the address has been validated, the **accountAuthToken** is generated. Save the generated token and select ![alt text](https://files.readme.io/b1609bfc8152341b73491d22eb12d4e9afd120ad0d5644d8bdb0f0dd82f7ee2b-Next_button.png).
6. At the **Multi Factor Authentication** stage, complete the multi-factor authentication process by using the **accountAuthToken** generated at the **Shipping Address** stage.
7. Once all the stages have been completed, select ![alt text](https://files.readme.io/de151504635fd8047fe8fb205e9722ac5f626457b36dfc580618e40a539af45a-Submit_button.png).

> 📘 *Note*
>
> *After submitting the form, if you have enabled the**Enable Electronic Trade Documents (ETD)** checkbox, then a corresponding dialog is displayed, prompting you to configure the ETD data via the [Signatures and logos](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) feature of SAPIENT.*

Once submitted and the desired ETL data is configured, your FedEx shipping account is created successfully. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account and start shipping with it.