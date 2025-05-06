---
title: Specify shipping account details
deprecated: false
hidden: true
metadata:
  robots: index
---
While creating a new FedEx shipping account in SAPIENT, at the **Shipping Account** stage, you can specify the general details associated to your FedEx account number.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/f09b766e605894fe2654059248e798b97d0255e3b4f8535c7ce81dc4893ed87a-FEDEX_Shipping_account_stage.png" />

The information on how to fill in the the necessary information at this stage are explained in the following table.

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
        **Carrier Account Number**\*
      </td>

      <td>
        Enter the 9-digit account number for FedEx.

        *`Note`: The carrier account number must be an exact match with what FedEx have provided.*
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)**\*
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type**\*
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
        **Alias**\*
      </td>

      <td>
        Enter a custom name which can be used when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name**\*
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number**\*
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
        Select this checkbox if you want to utilise electronic trade documents when shipping with FedEx. If you have completed the account creation process with this option selected, then at the end of the from, the system prompts you to go to the [Add signature and logo](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) page of the application to configure the required data for ETD.
      </td>
    </tr>

    <tr>
      <td>
        **Duties and taxes payment type**\*
      </td>

      <td>
        From the dropdown menu, select one of the following options:

        • **Sender** (a default value): The sender (or shipper) is responsible for any duties and taxes incurred when the <Glossary>shipment</Glossary> reaches its destination. This option is typically used when the sender wants full control over the shipment's costs.

        • **ThirdParty**: A third-party account is billed for duties and taxes. This option is used when the sender wants another designated company (not the sender or receiver) to pay the applicable fees. This means that the designated third party will bear the costs of duties and taxes instead of the sender or recipient.

        *`Note`: When the**ThirdParty** option is selected, an additional form is displayed for you to enter the third-party account details. For more information on how to fill this form, refer to the fields explained in the following table.*
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
        **Contact Name**
      </td>

      <td>
        Enter the name of the primary contact person associated with the third party account.
      </td>
    </tr>

    <tr>
      <td>
        **Company Name**
      </td>

      <td>
        Enter the name of the company associated with the third party account.
      </td>
    </tr>

    <tr>
      <td>
        **Country**
      </td>

      <td>
        From the dropdown menu, select the country in which the third party operates.
      </td>
    </tr>

    <tr>
      <td>
        **Address**\*
      </td>

      <td>
        Enter the first line of the third party's address, typically including the street address or location where the company is based. This is important for accurate delivery and communication.
      </td>
    </tr>

    <tr>
      <td>
        **Address 2**
      </td>

      <td>
        Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.
      </td>
    </tr>

    <tr>
      <td>
        **Address 3**
      </td>

      <td>
        Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.
      </td>
    </tr>

    <tr>
      <td>
        **Town**\*
      </td>

      <td>
        Enter the town or city where the third party company is located.
      </td>
    </tr>

    <tr>
      <td>
        **County**
      </td>

      <td>
        Enter the name of the county in which the the third party company is located.
      </td>
    </tr>

    <tr>
      <td>
        **Postcode**
      </td>

      <td>
        Enter the postal/ZIP code for the third party's address.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Phone**
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
        Select ![alt text](https://files.readme.io/b6c8af0dd2df7d574d6e95a6d57dee08b1b36bfe92e4350a94cb3b7eee6a5b71-Next_button.png) to proceed to the [Shipping Address](https://docs.intersoftsapient.net/docs/specify-shipping-address-details#/) stage of the form.
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

If the **Duties and taxes payment type** field is set to Third Party, then you are must fill the additional fields as explained in the following table.

<br />

|              Element             | Description                                                                                                                                                                                                                                          |
| :------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Third Party Account Number**\* | Enter the the unique FedEx account number of the third party that will be billed for the duties and taxes.                                                                                                                                           |
|         **Contact Name**         | Enter the name of the primary contact person associated with the third party account.                                                                                                                                                                |
|         **Company Name**         | Enter the name of the company associated with the third party account.                                                                                                                                                                               |
|            **Country**           | From the dropdown menu, select the country in which the third party operates.                                                                                                                                                                        |
|           **Address**\*          | Enter the first line of the third party's address, typically including the street address or location where the company is based. This is important for accurate delivery and communication.                                                         |
|           **Address 2**          | Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.                                                                    |
|           **Address 3**          | Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.                                                                                                                           |
|            **Town**\*            | Enter the town or city where the third party company is located.                                                                                                                                                                                     |
|            **County**            | Enter the name of the county in which the the third party company is located.                                                                                                                                                                        |
|           **Postcode**           | Enter the postal/ZIP code for the third party's address.                                                                                                                                                                                             |
|         **Contact Phone**        | Enter the phone number for the third party's primary contact person.                                                                                                                                                                                 |
| **Third Party Account Number**\* |                                                                                                                                                                                                                                                      |
| **Tax Identification Numbers**\* | Enter the third party's tax identification numbers (TINs). If there are multiple TINs that need to be provided, separate each ID with a comma. This information is often required for customs clearance and ensures compliance with tax regulations. |