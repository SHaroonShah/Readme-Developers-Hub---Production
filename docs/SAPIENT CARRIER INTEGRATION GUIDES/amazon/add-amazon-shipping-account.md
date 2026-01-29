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
    To add an On-Amazon shipping account in SAPIENT, perform the steps as explained in the following procedure.
<ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping accounts page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select the add shipping account button</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Accounts** page that opens, select the **Add Shipping Account** button.

        <Image align="center" border={true} src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
        <br />

        On the **Add Shipping Account** form that appears, fill in the **ACCOUNT DETAILS** block:

        <Image align="center" border={true} src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" alt="Entering account details" />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        | Element                 | Description                                                                                                   |
        | ----------------------- | ------------------------------------------------------------------------------------------------------------- |
        | **Carrier**\*           | From the dropdown list, select the carrier for which you want to add a shipping account.                      |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information:

        <Image align="center" border={true} src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" alt="Specifying shipping account details" />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        | Element                         | Description                                                                                                                                                                                      |
        | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
        | **Carrier Account Number**\*    | Enter the carrier account number. The format must be compliant with your selected carrier. Add leading zeros if needed to meet character length requirements                                     |
        | **Account Type**\*              | Select either [Production](https://docs.intersoftsapient.net/docs/sandbox-account) (live environment) or [Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account) (testing environment) |
        | **Account Name**\*              | Enter the account name if different from customer name                                                                                                                                           |
        | **Registered Email Address**\*  | Enter the email address used to register with the carrier                                                                                                                                        |
        | **Registered Billing Postcode** | Enter the postcode for billing.<br /> `Note`: *If you are unsure of the postcode, use the one shown on your invoice.*                                                                            |

        ### Contact Information

        | Element              | Description                                                                          |
        | -------------------- | ------------------------------------------------------------------------------------ |
        | **Alias**\*          | Enter a memorable custom name for API requests instead of using shipping location ID |
        | **Contact Name**\*   | Enter the primary contact name for this account                                      |
        | **Contact Number**\* | Enter the contact phone number for this account                                      |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, complete the carrier-specific fields.

        > 🚧 *Important*
        >
        > *The fields in this section vary depending on your selected carrier. Each carrier has unique requirements and authentication methods. To get more information on how to fill the fields in this block, refer to the[carrier specific guides](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/carrrier-specific-user-guides#/) section.*

        <br />

        After entering all the required information, select ![](https://files.readme.io/c8e36ac323cf6d3859bfa7081ee7ab63495ded4fd04cdb97aa685e06071cf4b4-add_shipping_account_button_2.png).
      </ToggleListItem>
    </ToggleList>
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

<Image align="center" alt="Entering account details" border={false} caption="Entering account details" src="https://files.readme.io/10427aae4b293b0b20082bb43c8049ae5ed57cf38f954946f530b23053d64864-Account_details_block_Amazon.png" width="500px" />

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                                   |
| :--------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier***      | From the dropdown list, select **AMAZON**.                                                                    |
| **Shipping Location*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/53a765a066729b4aa4b2d740073f4681bc75f021b3c396fd317e9ba810a2247b-Shipping_account_block_Amazon.png" width="600px" />

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

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/f43827dd6994b5da5d74fb6ec99a873e0386405a85d0769f4bb1d933e07e163e-carrier_details_block_On_Amazon.png" width="600px" />

6. After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).
7. In the **Shipping Account Added** dialog that appears, based on your preferences, proceed as follows.

<Image align="center" border={true} src="https://files.readme.io/7355f68879495a8c59f2ff1ef019fc1b924009ae7e9bbd4b57235553dfe18c5f-Shippig_account_confirmation_dialog_Amazon.png" className="border" />

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Button
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        ![](https://files.readme.io/1668b1ad81bff395a051eb64db26205ccc5635e2636194e1a5725b16156243c8-Connect_now_button.png)
      </td>

      <td>
        Select this button if you want to instantly connect this shipping account with your Amazon seller central account. Upon selection, you are directed to a new browser with the Amazon seller central login screen.

        Enter your login details and sign in to connect your shipping account with your Amazon seller central account.
      </td>
    </tr>

    <tr>
      <td>
        ![](https://files.readme.io/619a4b25c7ee5800144aa6889aa351de103c330e83f30fb8a818908e71e30df0-Connect_later_button.png)
      </td>

      <td>
        Select this button to save the shipping account without linking it to your Amazon seller central. This option creates your shipping account with a **Disabled** status and a connection status of **Not Connected**.

        You can connect the shipping account later by selecting this shipping account from the list and clicking ![](https://files.readme.io/8a55ea176fffa169c336d8f61757f2d9bafa0a91f6941c1eb10f1d66ed82b10d-Login_with_Amazon_button.png) provided in the **CARRIER DETAILS** block.
      </td>
    </tr>
  </tbody>
</Table>

Once the shipping account is connected, its account status moves to **Enabled**. You can now start shipping with it.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers">API References</Anchor> section._
