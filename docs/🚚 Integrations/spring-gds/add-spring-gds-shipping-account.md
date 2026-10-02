---
title: Add Spring GDS shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
icon: fad fa-square-plus
link:
  new_tab: false
metadata:
  robots: index
---
In SAPIENT, you can add a Spring GDS shipping account to a shipping location so that you can use it to create shipments.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you set up the account, [enable the label integration](https://docs.intersoftsapient.net/docs/integration-activation) for Spring GDS and [create a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
</Callout>

## How to add a Spring GDS shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    Follow these steps to add the account in SAPIENT.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select the option to add a shipping account">
        On the **Shipping Accounts** page, select ![](https://files.readme.io/a68fed3fbbb1668dedfcf9e0a5bd246f3f1dfa92bb6c7a47c175ad8df700e827-add_shipping_account_button.png).

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form, complete the **ACCOUNT DETAILS** block.

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :--- | :--- |
        | **Carrier**\* | Select Spring GDS from the dropdown list. |
        | **Shipping Location**\* | Select the shipping location you want to assign to this account. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the account information.

        <AsteridkForMandatoryElements />

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>Element</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>**Account Name (if different than customer)**\*</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td>**Account Type**\*</td>
              <td>Select **Production** for live shipping or **Sandbox** for testing. See [Sandbox account](https://docs.intersoftsapient.net/docs/sandbox-account) for details.</td>
            </tr>
            <tr>
              <td>**Alias**\*</td>
              <td>Enter a memorable name that you can use in an application programming interface (API) request instead of the shipping account ID.</td>
            </tr>
            <tr>
              <td>**Contact Name**\*</td>
              <td>Enter the contact name for the account.</td>
            </tr>
            <tr>
              <td>**Contact Number**\*</td>
              <td>Enter the contact number for the account.</td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the credentials for your Spring GDS account shown on the form.

        <Callout icon="📘" theme="info">
          ### _Note_

          _The existing Spring GDS guide contains InPost-specific credential names and screenshots. Those details have not been verified for Spring GDS, so this page does not identify particular Spring GDS credential fields or state that a carrier account number is unnecessary. Use the fields displayed for Spring GDS in SAPIENT and obtain the corresponding credentials from your Spring GDS account information._
        </Callout>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After completing the required fields, select ![](https://files.readme.io/7bacd208cbc1e3036e95df7c94e4b08f4f731910cf76b88ddd1eb137177b4018-add_shipping_account_button_2.png).

        When the account has been added, you can use it to create shipments.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    <Callout icon="📘" theme="info">
      ### _Note_

      _This documentation does not currently identify a Spring GDS-specific Add Account API endpoint. Do not use an InPost or UPS endpoint to add a Spring GDS account._
    </Callout>
  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square" target="_blank">
    Update or modify an existing shipping account.
  </Card>
</Cards>