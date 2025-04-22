---
title: Add DX Express shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a shipping account with DX, assign your DX credentials to it, and then link it to the relevant <Glossary>shipping location</Glossary>(s).

> 🚧 *Important*
>
> *Before you can set up a shipping account, make sure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for DX Express.*

To add a shipping account for DX in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/a2dad7052816bc2eb88dccddb82ee81753d9b31a2b436529e7ee59084897374d-Account_details_block_DX.png" width="500px" />

<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                   |
| :---------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier**\*      | From the dropdown list, select **DX**.                                                                        |
| **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/d0eae769c813147e1ba1ff428f31e2a84852aba1218a4858b7324d86458cd559-Shipping_account_block_DX.png" width="400px" />

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
        Enter the account number for DX

        *`Note`: If you already have an account with DX that is actively being used, and if you wish to receive tracking via Intersoft, then you need to request a new account number in order to integrate with Intersoft. This request can be made to your DX account manager.*
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

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Alias**\*
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
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
  </tbody>
</Table>

5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/fccccd4dc5ad4bc5f6a8bb8f7447d45b031f644466df17c80c3a9770a498fa66-carrier_details_block_DX.png" width="400px" />

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
        **DX Username**\*
      </td>

      <td>
        Enter your DX username.

        *`Note`: This information is your DX API credentials. For more information on how to create the API credentials, refer to the**[Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials) \*\* section.*
      </td>
    </tr>

    <tr>
      <td>
        **DX Password**\*
      </td>

      <td>
        Enter your DX password.

        *`Note`: This information is your DX API credentials. For more information on how to create the API credentials, refer to the**[Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials)  \*\* section.*
      </td>
    </tr>
  </tbody>
</Table>

6. After entering all the required information, select ![alt text](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

> 📘 *Note*
>
> *Shipping account(s) can be added and managed via API. For more information, refer to the[API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section.*

### See also

* [DX Express sign-off](https://docs.intersoftsapient.net/docs/dx-freight-sign-off-copy)
* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)