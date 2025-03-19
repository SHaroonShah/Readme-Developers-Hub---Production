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
> * *The exact shipping address that you have provided to FedEx, as this information is validated via the Address Validation API. If the address does not match, then a corresponding error message is displayed—and you will not proceed to the**Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form.*

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
6. At the Multi Factor Authentication stage, complete the multi-factor authentication process by using the **accountAuthToken** generated at the **Shipping Address** stage.
7. Once all the stages have been completed, select ![alt text](https://files.readme.io/de151504635fd8047fe8fb205e9722ac5f626457b36dfc580618e40a539af45a-Submit_button.png).

> 📘 *Note*
>
> *After submitting the form, if you have enabled the**Enable Electronic Trade Documents (ETD)** checkbox, then a corresponding dialog is displayed, prompting you to configure the ETD data via the [Signatures and logos](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) feature of SAPIENT.*

4. Once submitted and the desired ETL data is configured, your FedEx shipping account is created successfully. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account and start shipping with it.
5. In the **CONNECT YOUR FEDEX ACCOUNT** form that appears, at the **Shipping Account** stage, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/fa447171e8f90a43d206fa93b5dacfb723a09dca86dd4b979c21153c4a169bda-FEDEX_Shipping_account_stage.png" />

> 💡 *Tip*
>
> *In the following table, the mandatory fields are marked with an asterisk (\*).*

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
        **Carrier Account Number\***
      </td>

      <td>
        Enter the 9-digit account number for FedEx.

        *`Note`: The carrier account number must be an exact match with what FedEx have provided.*
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)\***
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type\***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users. When you select **Production**, then upon selecting ![alt text](https://files.readme.io/9a8ec72b5969b1f4747f125dbf2e278b2442e39cb1dfe637a2d635f6020db504-Next_button.png), you are proceeded to the next stages of the form for the address and MFA validation processes.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes. If you select the **Sandbox** environment, then the shipping account is created without the address and MFA validation processes.

        *`Note`: You can use the**Sandbox** account to test the integration and generate test labels to ensure that it is configured correctly.*
      </td>
    </tr>

    <tr>
      <td>
        **Alias\***
      </td>

      <td>
        Enter a custom name which can be used when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name\***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number\***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Enable Electronic Trade Documents (ETD)**
      </td>

      <td>
        Select this checkbox if you want to utilise electronic trade documents when shipping with FedEx. When this option is selected, you are prompted and redirected to the [Add signature and logo](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) page of the application, where you can configure the required data for ETD.
      </td>
    </tr>

    <tr>
      <td>
        **Duties and taxes payment type**
      </td>

      <td>
        From the dropdown menu, select one of the following options:

        • **Sender** (a default value): The sender (or shipper) is responsible for any duties and taxes incurred when the <Glossary>shipment</Glossary> reaches its destination. This option is typically used when the sender wants full control over the shipment's costs.

        • **ThirdParty**: A third-party account is billed for duties and taxes. This option is used when the sender wants another designated company (not the sender or receiver) to pay the applicable fees. This means that the designated third party will bear the costs of duties and taxes instead of the sender or recipient.

        *`Note`: When the**ThirdParty** option is selected, an additional form is displayed for you to enter the third-party account details. For more information on how to fill this form, refer to the fields explained below.*
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Account Number**\*
      </td>

      <td>
        Enter the the unique FedEx account number of the third party that will be billed for the duties and taxes.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Contact Name**
      </td>

      <td>
        Enter the name of the primary contact person associated with the third party account.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Company Name**
      </td>

      <td>
        Enter the name of the company associated with the third party account.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Address Line 1**\*
      </td>

      <td>
        Enter the first line of the third party's address, typically including the street address or location where the company is based. This is important for accurate delivery and communication.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Address Line 2**
      </td>

      <td>
        Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Address Line 3**
      </td>

      <td>
        Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Town**\*
      </td>

      <td>
        Enter the town or city where the third party company is located.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Country**\*
      </td>

      <td>
        Enter country in which the third party company operates.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Postcode**
      </td>

      <td>
        Enter the postal/ZIP code for the third party's address.
      </td>
    </tr>

    <tr>
      <td>
        **Third Party Contact Phone**
      </td>

      <td>
        Enter the phone number for the third party's primary contact person.
      </td>
    </tr>

    <tr>
      <td>
        **Tax Identification Numbers**\*
      </td>

      <td>
        Enter the third party's tax identification numbers (TINs). If there are multiple TINs that need to be provided, separate each ID with a comma. This information is often required for customs clearance and ensures compliance with tax regulations.
      </td>
    </tr>

    <tr>
      <td>
        **Next**
      </td>

      <td>
        Select ![alt text](https://files.readme.io/b6c8af0dd2df7d574d6e95a6d57dee08b1b36bfe92e4350a94cb3b7eee6a5b71-Next_button.png) to proceed to the Shipping Address stage of the form.
      </td>
    </tr>

    <tr>
      <td>
        **Submit**
      </td>

      <td>
        Select ![alt text](https://files.readme.io/2ffa9cf28233588e3fa0be9258d8a2d6f5aa9d84f5e25f263c2c4d8c214cdbba-Submit_button.png) to create the shipping account and close the form.\
        *`Note`: This button is only displayed if you have selected the**Sandbox** <Glossary>account type</Glossary>.*
      </td>
    </tr>
  </tbody>
</Table>