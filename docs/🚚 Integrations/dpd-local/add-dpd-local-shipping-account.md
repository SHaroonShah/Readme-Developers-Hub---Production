---
title: Add DPD Local shipping account
deprecated: false
hidden: true
metadata:
  robots: index
---
In SAPIENT, you can create a DPD Local shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have&#x20;_[_enabled the label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;for DPD Local and have already&#x20;_[_created a shipping location_](https://docs.intersoftsapient.net/docs/add-a-shipping-location)_._
</Callout>

## How to add DPD Local shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a DPD Local shipping account via SAPIENT UI, perform the steps as explained in the following procedure:

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page" icon="fa-mouse-pointer">

        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="fa-plus">

        <br />

        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" caption="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="fa-file-alt">

        <br />

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image src="https://files.readme.io/0bf771710894e28b32544ee1d8bf0234b879666a0e78f4accc9223fa557b8275-image.png" align="center" caption="Entering account details" border={true} />

        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select DPD Local as your carrier option.                                                                    |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="fa-box">

        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image src="https://files.readme.io/c9ba2c7e217fe95baa32302ba11066d8a351c94cc67683ae26207a62dd1ae77f-image.png" align="center" caption="Entering shipping account details" border={true} />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            
            <tr>
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
              </td>
            </tr>
            <tr>
              <td><strong>Alias</strong>&#42;</td>
              <td>Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.</td>
            </tr>
            <tr>
              <td><strong>Contact Name</strong>&#42;</td>
              <td>Enter the contact name for the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Contact Number</strong>&#42;</td>
              <td>Enter the contact number for the account you are adding.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details" icon="fa-truck">

        <br />

        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image src="https://files.readme.io/debe2eee0ec10c04b070243818f709eb03568261c4642c3cdb6170f6eb3e36fb-image.png" align="center" caption="Entering carrier-specific details" />

        <br />

        <AsteridkForMandatoryElements />

        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>API Key</strong>&#42;</td>
              <td>
                Enter the API Key provided by DPD Local for authetnicating the API requests.
                <br />
              </td>
            </tr>
            <tr>
              <td><strong>API Secret</strong>&#42;</td>
              <td>Enter the API Secrect for the enetered API Key provided by DPD Local.</td>
            </tr>
          </tbody>
        </table>
    <br />

    > 📘 *Note*
        >
        > *The **API Key** and **API Secret** credentials must be separate for Sandbox and Production accounts.*
        ***

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account" icon="fa-check">

        <br />

        After entering all the required information, select ![](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DPD Local shipping account via API, refer to the following API endpoint.

    <Cards columns="2">
      <Card title="Add Account" icon="fa-code" target="_blank">
        Add and manage DPD Local shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square" target="_blank">
    Update or modify an existing shipping account.
  </Card>
</Cards>
