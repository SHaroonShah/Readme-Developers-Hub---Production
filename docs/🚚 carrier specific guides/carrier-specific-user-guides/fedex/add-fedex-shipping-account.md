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

4. In the **CONNECT YOUR FEDEX ACCOUNT** form that appears, at the **Shipping Account** stage, enter the necessary information as explained in the following table.

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
        **Duties and taxes payment type**
      </td>

      <td>
        From the dropdown menu, select one of the following options:

        • **Sender**: The sender (or shipper) is responsible for any duties and taxes incurred when the <Glossary>shipment</Glossary> reaches its destination. This option is typically used when the sender wants full control over the shipment's costs.

        • **ThirdParty**: A third-party account is billed for duties and taxes. This option is used when the sender wants another designated company (not the sender or receiver) to pay the applicable fees. This means that the designated third party will bear the costs of duties and taxes instead of the sender or receipient.

        *`Note`: When the**ThirdParty** option is selected, an additional form is displayed for you to enter the third-party account details.*
      </td>
    </tr>

    <tr>
      <td>
        **Enable Electronic Trade Documents (ETD)**
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/3707bf4d346ea1f22c7d1d3be7bf1d030ca19d84c84998da95fc31d47eb8fc70-carrier_details_block_DX_Freight.png" width="400px" />

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
        **Origin Service Centre (Also referred to as "Depot")\***
      </td>

      <td>
        Enter the origin service code for identifying the correct physical location from which the <Glossary>shipments</Glossary> originate.

        *`Note`: This code may vary depending on the selected service type, for example it can be a single number or a combination of  two letters and numbers. For more information, please contact DX Freight.*
      </td>
    </tr>

    <tr>
      <td>
        **Password\***
      </td>

      <td>
        Enter the password associated with your DX Freight account. It is essential for securing the account and ensuring that only authorized users have access to shipping details and operations.
      </td>
    </tr>

    <tr>
      <td>
        **Service Type\***
      </td>

      <td>
        From the dropdown menu, select one the following service types that you want to use for your shipments, specifically in terms of the number of personnel involved in the delivery:

        • **1 Man**: This service type typically means that one crew member will handle the delivery. This is suitable for smaller, lighter <Glossary>items</Glossary> that one person can manage without assistance.

        • **2 Man**: This indicates that two personnel will be involved in the delivery process, which is often necessary for larger or heavier items that require additional handling or lifting.

        *`Note`: Bear in mind that you need to create separate shipping accounts for each service type that you wish to use in your shipments.*
      </td>
    </tr>
  </tbody>
</Table>

6. After entering all the required information, select ![alt text](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.