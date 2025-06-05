---
title: Add The Delivery Group shipping account
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
In SAPIENT, you can create a shipping account with The Delivery Group (TDG), and then link it to the relevant <Glossary>shipping location</Glossary>(s).

As a TDG customer, you must follow the following prerequisites before onboarding with Intersoft:

1. First, you need to contact the TDG sales team to discuss and agree on commercial terms and participate in initial onboarding discussions.
2. Once the commercial agreement is in place, the Sales Account Manager will forward the account to the TDG Onboarding team, where an Onboarding Manager will be assigned to you.
3. After, The TDG Onboarding team will assign and provide the you with the necessary API credentials required for connecting to Intersoft.

> 🚧 *Important*
>
> *After you have received the API credentials from TDG, you can now set up a shipping account on SAPIENT. Before doing that, make sure you have[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with The Delivery Group and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location).*

To add a shipping account for The Delivery Group in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/f979b6d755483ee5fc3af33e47c43bbdf078b633d3b3fb581e0e0baf1e209b85-Account_details_block_TDG.png" width="500px" />

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
        **Carrier**\*
      </td>

      <td>
        From the dropdown list, select **TDG - The Delivery Group**.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Location**\*
      </td>

      <td>
        From the dropdown menu, select the location that you want to assign to the shipping account you are creating.

        *`Note`: Before selecting the shipping location, make sure you have[created one](https://docs.intersoftsapient.net/docs/add-a-shipping-location) beforehand.*
      </td>
    </tr>
  </tbody>
</Table>

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/12ec9fe8afb8e032cec6894c74922036fc43d0290e2b288af427a0a6c6689d06-Shipping_account_block_TDG.png" width="400px" />

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
        Enter the account number for The Delivery Group.

        The format of the account number must be compliant with the carrier you have selected.
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)**\*
      </td>

      <td>
        Enter the client name allocated to you by The Delivery Group.
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

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/8dbf30060f2fe9a26e0b63a6a82fa6402ff99ed4d4c3e4f87547b240dd441c55-carrier_details_block_TDG.png" width="400px" />

<AsteridkForMandatoryElements />

|              Element              | Description                                                                                                                                                                                     |
| :-------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **The Delivery Group Username**\* | Enter the user name that is registered with The Delivery Group.                                                                                                                                 |
| **The Delivery Group Password**\* | Enter the password associated with The Delivery Group account. It is essential for securing the account and ensuring that only authorized users have access to shipping details and operations. |

6. After entering all the required information, select ![alt text](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

> 📘 *Note*
>
> *Shipping account(s) can be added and managed via API. For more information, refer to the[API References](https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-tdg#/) section.*

### See also

* [The Delivery group sign-off](https://docs.intersoftsapient.net/docs/dx-freight-sign-off)
* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)