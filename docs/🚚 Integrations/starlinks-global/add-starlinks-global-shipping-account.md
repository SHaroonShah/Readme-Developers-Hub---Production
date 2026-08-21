---
title: Add Starlinks Global shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, with **the Add Shipping Account** functionality, you can select the desired shipping location and then add a Starlinks Global shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have enabled the&#x20;_[_label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;for Starlinks Global._
</Callout>

## How to add Starlinks Global shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for Starlinks Global in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Access the Shipping Accounts page">

        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" align="center" caption="Accessing shipping accounts" border={true} />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">

        <br />

        On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/a68fed3fbbb1668dedfcf9e0a5bd246f3f1dfa92bb6c7a47c175ad8df700e827-add_shipping_account_button.png).

        <Image src="https://files.readme.io/e0071b9f348522956cf0d9db5802f5bef56a11c5d3ff90f8a6bbedbc3c48d560-Add_shipping_account_button_UPS.png" alt="Accessing option to add shipping account" align="center" caption="Selecting option to add shipping account" border={true} />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">

        <br />

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image src="https://files.readme.io/0e740a5d4febd2dae888888ec78a9c3c7cc47c554e0d805db25abf5024ba1748-image.png" align="center" width="500px" caption="Entering account details" border={true} />

        <br />

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :--- | :--- |
        | **Carrier**\* | From the dropdown list, select **Starlinks Global**. |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">

        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image src="https://files.readme.io/72fbb84372b1189f1484466e78ee630740771119599185209582831a505f19b0-image.png" align="center" width="500px" caption="Entering shipping account details" border={true} />

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
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                <p>From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:</p>
                <ul>
                  <li><strong><a href="https://docs.intersoftsapient.net/docs/sandbox-account">Production</a></strong>: a live environment where the final version of the application is deployed and made available to the users.</li>
                  <li><strong><a href="https://docs.intersoftsapient.net/docs/sandbox-account">Sandbox</a></strong>: a testing environment that mimics the <strong>Production</strong> environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.</li>
                </ul>
              </td>
            </tr>
            <tr>
              <td><strong>Alias</strong>&#42;</td>
              <td>Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.</td>
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

      <ToggleListItem title="5. Enter carrier details">

        <br />

        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image src="https://files.readme.io/fea1554dd281c7a9c5b014dcfb1c3fa724d2b63043a3b8ed4a80233d8f96b788-image.png" align="center" width="500px" caption="Entering carrier-specific details" border={true} />

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
              <td>Enter the API key for the user account associated with Starlinks Gobal.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">

        <br />

        After entering all the required information, select ![alt text](https://files.readme.io/7bacd208cbc1e3036e95df7c94e4b08f4f731910cf76b88ddd1eb137177b4018-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a Starlinks Global shipping account via API, refer to the API References section.

    <Cards columns="2">
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-starlinks" icon="fa-code" target="_blank">
        Add and manage Starlinks Global shipping account via API.
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
