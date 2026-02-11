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
In SAPIENT, you can create both <Glossary>On-Amazon</Glossary> and <Glossary>Off-Amazon</Glossary> shipping accounts by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for Amazon._
>
> _Once the Amazon integration is activated, please bear in mind the following:_
>
> * _You cannot switch between On‑Amazon and Off‑Amazon shipping accounts after they have been created.._
> * _You can add and manage the shipping accounts via API, but you must log into the SAPIENT UI and complete the Login With Amazon (LWA) process._
>
> _For more information on how to add and manage shipping accounts via the API, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-carriers) section._

To add a shipping account for Amazon in SAPIENT, follow the instructions as explained in the following procedures for each account type.

## How to add Amazon shipping account via UI

<Tabs>
  <Tab title="Add On-Amazon shipping account">
    To add an On-Amazon shipping account to SAPIENT, perform the steps as explained in the following procedure.

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

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/10427aae4b293b0b20082bb43c8049ae5ed57cf38f954946f530b23053d64864-Account_details_block_Amazon.png" width="500px" alt="Entering account details" />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **AMAZON**.                                                                    |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/53a765a066729b4aa4b2d740073f4681bc75f021b3c396fd317e9ba810a2247b-Shipping_account_block_Amazon.png" width="600px" alt="Specifying shipping account details" />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
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

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, expand the **Amazon Account Type** dropdown field and select **On Amazon**.

        > 🚧 *Important*
        >
        > *Use this block only if you have set your account type to**Production**. This block does not apply to the shipping accounts created with the **Sandbox** account type.*

        <Image align="center" border={true} src="https://files.readme.io/f43827dd6994b5da5d74fb6ec99a873e0386405a85d0769f4bb1d933e07e163e-carrier_details_block_On_Amazon.png" width="600px" alt="Entering carrier details" />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Save and add shipping account</strong>} icon="fa-rocket">
        <br />

        After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>7. Connect shipping account with your Amazon account</strong>} icon="fa-rocket">
        <br />

        In the **Shipping Account Added** dialog that appears, based on your preferences, proceed as follows.

        <Image align="center" border={true} src="https://files.readme.io/7355f68879495a8c59f2ff1ef019fc1b924009ae7e9bbd4b57235553dfe18c5f-Shippig_account_confirmation_dialog_Amazon.png" />

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

                <Image align="center" src="https://files.readme.io/8f06734f14e98a0fe80890254ce53e2abc2cfd8c442b96a4e49979376d0d033a-Amazon_seller_central_dialog.png" width="200px" />

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

                <Image align="center" src="https://files.readme.io/d0fd1abff3fd7f3a592d47fec656a50a71b6eae4424782f59d58f450eec95988-Selecting_login_with_Amazon_button.png" width="200px" />
              </td>
            </tr>
          </tbody>
        </Table>

        <br />

        Once the shipping account is connected successfully, its status moves to **Enabled**. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add Off-Amazon shipping account">
    To add an Off-Amazon shipping accoun to SAPIENT, perform the steps as explained in the following prcedure.

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

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/10427aae4b293b0b20082bb43c8049ae5ed57cf38f954946f530b23053d64864-Account_details_block_Amazon.png" width="500px" alt="Entering account details" />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **AMAZON**.                                                                    |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/53a765a066729b4aa4b2d740073f4681bc75f021b3c396fd317e9ba810a2247b-Shipping_account_block_Amazon.png" width="600px" alt="Specifying shipping account details" />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
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

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, expand the **Amazon Account Type** dropdown field and select **Off Amazon**.

        > 🚧 *Important*
        >
        > *Use this block only if you have set your account type to**Production**. This block does not apply to the shipping accounts created with the **Sandbox** account type.*

        <Image align="center" src="https://files.readme.io/387253706a2df3ada57a5aa57ac517af6f17b943f7660795133f67edc54e2d78-carrier_details_block_Off_Amazon.png" width="600px" />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Save and add shipping account</strong>} icon="fa-rocket">
        <br />

        After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>7. Connect shipping account with your Amazon account</strong>} icon="fa-rocket">
        <br />

        In the **Shipping Account Added** dialog that appears, based on your preferences, proceed as follows.

        <Image align="center" border={true} src="https://files.readme.io/7355f68879495a8c59f2ff1ef019fc1b924009ae7e9bbd4b57235553dfe18c5f-Shippig_account_confirmation_dialog_Amazon.png" />

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
                Select this button if you want to instantly connect this shipping account with your Amazon shipping account. Upon selection, you are directed to a new browser with the Amazon shipping login screen.

                <Image align="center" src="https://files.readme.io/b936abb006f01c8213b8911fd872052ac97979c8dc81457f1364468795245122-Amazon_shipping_dialog.png" width="200px" />

                Enter your login details and sign in to connect your shipping account with your Amazon shipping account.
              </td>
            </tr>

            <tr>
              <td>
                ![](https://files.readme.io/619a4b25c7ee5800144aa6889aa351de103c330e83f30fb8a818908e71e30df0-Connect_later_button.png)
              </td>

              <td>
                Select this button to save the shipping account without linking it to your Amazon shipping account. This option creates your shipping account with a **Disabled** status and a connection status of **Not Connected**.

                You can connect the shipping account later by selecting this shipping account from the list and clicking ![](https://files.readme.io/8a55ea176fffa169c336d8f61757f2d9bafa0a91f6941c1eb10f1d66ed82b10d-Login_with_Amazon_button.png) provided in the **CARRIER DETAILS** block.

                <Image align="center" src="https://files.readme.io/d0fd1abff3fd7f3a592d47fec656a50a71b6eae4424782f59d58f450eec95988-Selecting_login_with_Amazon_button.png" width="200px" />
              </td>
            </tr>
          </tbody>
        </Table>

        <br />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>8. Authorise your account</strong>} icon="fa-rocket">
        <br />

        In the authorisation page that opens, select the checkbox if you agree with the authorisation terms, select ![alt text](https://files.readme.io/3f6f67356aa9dca354db43483cb3e1c8739ed9112f2ce231fcef754fd3175f1a-Authorise_button.png).

        <Image align="center" src="https://files.readme.io/1377e7ba5e9d77c6a21cbfbc1838eaf509e30694fa8e8665be5100efd27bd1b2-Authorise_screen_Amazon_Off.png" width="500px" />

        Once the shipping account is connected successfully, its status moves to **Enabled**. You can now start shipping with it.

        <Image align="center" src="https://files.readme.io/08218f7241ea7b5336492b77d5bcbdc9303edca583575035c065a6d60cd784a0-Activate_and_enabled_Amazon_Off_account.png" />

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>
</Tabs>

> 📘 _Note_
>
> _Once the Amazon integration is activated, please bear in mind the following:_
>
> * _You cannot swap between the On-Amazon and Off-Amazon shipping accounts after their creation._
> * _You can add and manage the shipping accounts via <Anchor label="API" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers">API</Anchor>, but you first need to log into the SAPIENT UI and complete the Login With Amazon (LWA) process._

***

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)

<br />
