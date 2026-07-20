---
title: Add DX Express shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a DX Express shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have performed the following operations:_
>
> 1. _[Enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for DX Express and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
> 2. _Created and obtained the [DX API credentials](https://docs.intersoftsapient.net/v4.03/docs/setting-up-dx-api-credentials)_

## How to add DX Express shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for DX Express in SAPIENT, follow the instructions as explained in the following procedure:

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page " icon="list-ol">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="list-ol">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" caption="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="list-ol">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/a2dad7052816bc2eb88dccddb82ee81753d9b31a2b436529e7ee59084897374d-Account_details_block_DX.png" width="500px" caption="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **DX**.                                                                        |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="list-ol">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/d0eae769c813147e1ba1ff428f31e2a84852aba1218a4858b7324d86458cd559-Shipping_account_block_DX.png" width="400px" caption="Specifying shipping account details" />

        <br />

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

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details" icon="list-ol">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/fccccd4dc5ad4bc5f6a8bb8f7447d45b031f644466df17c80c3a9770a498fa66-carrier_details_block_DX.png" width="400px" caption="Entering carrier details" />

        <br />

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

                *`Note`: This information is your DX API credentials. For more information on how to create the API credentials, refer to the*\_[Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials) \*\* section.\_
              </td>
            </tr>

            <tr>
              <td>
                **DX Password**\*
              </td>

              <td>
                Enter your DX password.

                *`Note`: This information is your DX API credentials. For more information on how to create the API credentials, refer to the*\_[Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials)  \*\* section.\_
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account" icon="list-ol">
        After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DX Express shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dx" icon="fa-code">
        Add and manage DX Express shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={3}>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off">
    Update or modify an existing shipping account.
  </Card>

  <Card title="DX Express Sign-Off" icon="fa-solid fa-file-signature" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off-copy">
    Complete necessary steps before using DXF to create shipments in SAPIENT.
  </Card>

  <Card title="DX Rate Limit" icon="fa-solid fa-file-signature" href="https://docs.intersoftsapient.net/v4.03/docs/dx-rate-limit">
    Learn more about the DX rate limit set on the number of requests that can be processed over a given period of time.
  </Card>
</Cards>