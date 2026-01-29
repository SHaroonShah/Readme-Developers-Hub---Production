---
title: Add Amazon shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
metadata:
  robots: index
---
In SAPIENT, you can create <Glossary>On-Amazon</Glossary> and <Glossary>Off-Amazon</Glossary>shipping accounts and then link it to the relevant <Glossary>shipping location</Glossary>(s).

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for Amazon._

To add a shipping account for Amazon in SAPIENT, follow the instructions as explained in the following procedures for each account type.

<Tabs>
  <Tab title="Add On-Amazon shipping account">
    Welcome to the content that you can only see inside the first Tab.
  </Tab>

  <Tab title="Add Off-Amazon shipping account">
    Here's content that's only inside the second Tab.
  </Tab>
</Tabs>

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/10427aae4b293b0b20082bb43c8049ae5ed57cf38f954946f530b23053d64864-Account_details_block_Amazon.png" width="500px" />

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                                   |
| :--------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier***      | From the dropdown list, select **AMAZON**.                                                                    |
| **Shipping Location*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/53a765a066729b4aa4b2d740073f4681bc75f021b3c396fd317e9ba810a2247b-Shipping_account_block_Amazon.png" width="400px" />

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory fields are marked with an asterisk (*)._
</Callout>

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
        **Account Name (if different than customer)***
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Alias***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

5. In the **CARRIER DETAILS** block, expand the **Amazon Account Type** dropdown field and select **On Amazon**.

> 🚧 _Important_
>
> _Use this block only if you have set your account type to **Production**. This block does not apply to the shipping accounts created with the **Sandbox** account type._

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/f43827dd6994b5da5d74fb6ec99a873e0386405a85d0769f4bb1d933e07e163e-carrier_details_block_On_Amazon.png" width="400px" />

6. After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).
7. In the **Shipping Account Added** dialog that appears, based on your preferences, proceed as follows:
   1. ![](https://files.readme.io/1668b1ad81bff395a051eb64db26205ccc5635e2636194e1a5725b16156243c8-Connect_now_button.png): Select this button if you want to instantly connect this shipping account with your Amazon seller central account. Upon selection, you are directed to the
   2. ![](https://files.readme.io/b737cad7a32d0b1390e7ba4b050cea234123af9a0baf7895c5080809ab367265-Connect_later_button.png):

Once done, you have now successfully added a shipping account. You can now start shipping with it.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers">API References</Anchor> section._
