---
title: Add The Delivery Group shipping account
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
In SAPIENT, you can create a The Delivery Group (TDG) shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have performed the following operations:_

  1. _Contacted the TDG sales team to discuss and agree on commercial terms and participate in initial onboarding discussions._
  2. _Confirmed that the Sales Account Manager has forwarded the account to the TDG Onboarding team, where an onboarding Manager will be assigned to you._
  3. _Received the necessary API credentials from the TDG Onboarding team for connecting to Intersoft._
  4. _[Enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for The Delivery Group and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
</Callout>

## How to add The Delivery Group shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for The Delivery Group in SAPIENT, perform the steps as explained in the following procedure:

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page " icon="list-ol">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="list-ol">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" caption="Selecting option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="list-ol">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/f979b6d755483ee5fc3af33e47c43bbdf078b633d3b3fb581e0e0baf1e209b85-Account_details_block_TDG.png" width="500px" caption="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **TDG - The Delivery Group**.                                                  |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="list-ol">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/12ec9fe8afb8e032cec6894c74922036fc43d0290e2b288af427a0a6c6689d06-Shipping_account_block_TDG.png" width="400px" caption="Entering shipping account details" />

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

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: A live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: A testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
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

        <Image align="center" border={true} src="https://files.readme.io/8dbf30060f2fe9a26e0b63a6a82fa6402ff99ed4d4c3e4f87547b240dd441c55-carrier_details_block_TDG.png" width="400px" caption="Entering carrier-specific details" />

        <br />

        <AsteridkForMandatoryElements />

        |              Element              | Description                                                                                                                                                                                     |
        | :-------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | **The Delivery Group Username**\* | Enter the user name that is registered with The Delivery Group.                                                                                                                                 |
        | **The Delivery Group Password**\* | Enter the password associated with The Delivery Group account. It is essential for securing the account and ensuring that only authorized users have access to shipping details and operations. |

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
    To add The Delivery Group shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="API References" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-tdg" icon="fa-code">
        Add and manage The Delivery Group shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={3}>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/edit-shipping-account">
    Update or modify an existing shipping account.
  </Card>

  <Card title="The Delivery Group sign-off" icon="fa-solid fa-file-signature" href="https://docs.intersoftsapient.net/docs/the-delivery-group-sign-off#/">
    Complete the sign-off process before using The Delivery Group to create shipments in SAPIENT.
  </Card>

  <Card title="API References" icon="fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-tdg">
    Add and manage The Delivery Group shipping account via API.
  </Card>
</Cards>

<br />
