---
title: Add DPD NL shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, with the Add Shipping Account functionality, you can select the desired shipping location and then add a DPD NL shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have enabled the <Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for DPD NL and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
</Callout>

## How to add DPD NL shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for DPD NL in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/3a455e2719e4881e477bf78f117fa269ddb148a02a7dbd95daf3fdb49afdf456-image.png" width="500px" />

       <br />

        <AsteridkForMandatoryElements />

        | Element                 | Description                                                                                                   |
        | :---------------------- | :------------------------------------------------------------------------------------------------------------ |
        | **Carrier**\*           | From the dropdown list, select **DPD Netherlands**.                                                           |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/038ffd980b7ea30489f1537526e454561ca8b4c6207f368f198f7b3a796b76ba-image.png" width="500px" />

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
                Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
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

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/50b1c2b340debdfc89d6ac4056545f954a35b3025eac1f05cc88699c6e481523-image.png" width="600px" />

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
                **DPD Netherlands User ID**\*
              </td>

              <td>
                Enter unique identifier for the user account associated with DPD Netherlands.
              </td>
            </tr>

            <tr>
              <td>
                **DPD Netherlands Password**
              </td>

              <td>
                Enter the secure password used to authenticate the user account with DPD Netherlands.
              </td>
            </tr>

            <tr>
              <td>
                **DPD Netherlands Depot Number**
              </td>

              <td>
                Enter the unique 4-digit identifier for the specific depot or location where the shipment will be processed.
              </td>
            </tr>

            <tr>
              <td>
                **DPD Netherlands Notification Language**\*
              </td>

              <td>
                Enter the language code used for DPD Netherlands delivery notifications to be sent via Email or SMS—provided in the ISO 3166-1 alpha-2 format, for example, English, Dutch, and French.

                `Note`: *The notifications are only sent if either the Email or SMS enhancement code is provided in the create shipment request.*
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DPD NL shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dpdnl" icon="fa-code">
        Add and manage DPD NL shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={2}>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/edit-shipping-account">
    Update or modify an existing shipping account.
  </Card>
</Cards>

<br />
