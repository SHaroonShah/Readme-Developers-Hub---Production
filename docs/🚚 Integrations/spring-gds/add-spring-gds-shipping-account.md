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
In SAPIENT, you can select a shipping location and add a Spring GDS shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before setting up the account,&#x20;_[enable the label integration](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;for Spring GDS and&#x20;_[create a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)_._
</Callout>

## How to add a Spring GDS shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    Follow these steps to add a Spring GDS shipping account in SAPIENT.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

        <Image align="center" src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" caption="Selecting the option to add a shipping account (example carrier shown)" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form, in the **ACCOUNT DETAILS** block, enter the information in the following table.

        <Image align="center" src="https://files.readme.io/8c5d5f5ff0cecf1feaa16ffc521a0feaf02bffc8c255c4ab9d967f4ad6bdf203-Account_details_block_Inpost.png" width="500px" caption="Account details block (InPost example; select Spring GDS instead)" />

        <br />

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :--- | :--- |
        | **Carrier**\* | Select Spring GDS from the dropdown list. |
        | **Shipping Location**\* | Select the shipping location to assign to the account. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the information in the following table.

        <Image align="center" src="https://files.readme.io/aab73fec0c0be8505e9adce3450d783ae7d9f8ed4c7a9c0b9198b4682fb89679-Shipping_account_block_INPOST.png" width="500px" caption="Shipping account block (InPost example; Spring GDS fields may differ)" />

        <br />

        <Callout icon="💡" theme="default">
          ### _Tip_

          _Mandatory fields in the following table are marked with an asterisk (\*)._
        </Callout>

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
              <td>Select **Production** for live use or **Sandbox** for testing. See [Sandbox account](https://docs.intersoftsapient.net/docs/sandbox-account) for details.</td>
            </tr>
            <tr>
              <td>**Alias**\*</td>
              <td>Enter a memorable name to use in an application programming interface (API) request instead of the shipping account ID.</td>
            </tr>
            <tr>
              <td>**Contact Name**\*</td>
              <td>Enter the account contact’s name.</td>
            </tr>
            <tr>
              <td>**Contact Number**\*</td>
              <td>Enter the account contact’s telephone number.</td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the credentials for your Spring GDS account.

        <Image align="center" src="https://files.readme.io/3a5f6be5d0522b615c12181f01d628650d3ef6d3966de74d012fce372c78a302-carrier_details_block_InPost.png" width="400px" caption="Carrier details block (InPost example; use the fields shown for Spring GDS in SAPIENT)" />

        <br />

        <AsteridkForMandatoryElements />

        <Callout icon="📘" theme="info">
          ### _Note_

          _Spring GDS credential field names and account-number requirements have not been confirmed in this guide. Check the required fields displayed for Spring GDS in the form and obtain those credentials from your Spring GDS account contact. Do not use InPost credentials._
        </Callout>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering the required information, select the Add Shipping Account button.

        <Image align="center" src="https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png" />

        The account is ready to use when it appears on the **Shipping Accounts** page.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">

  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square" target="_blank">
    Update or modify an existing shipping account.
  </Card>
</Cards>
