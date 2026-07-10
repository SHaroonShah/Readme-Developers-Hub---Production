---
title: Add An Post shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, you can create an An Post shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warning">
  ### _Important_

  _Before you can set up a shipping account, make sure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with An Post and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
</Callout>

## How to add An Post shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    

    To add an An Post shipping account via SAPIENT UI, perform the steps as explained in the following procedure:

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page" icon="fa-arrow-pointer">

        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="fa-plus">

        <br />

        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="fa-address-card">

        <br />

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/bd4c02b7c9c557a48c13a92f58a9454ab0a5f8eb3aabdd462f6eba7147730d7d-Account_details_block_An_post.png" width="500px" alt="Entering account details" />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                                                 |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **ANPOST - An Post**.                                                                                        |
        | **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="fa-truck">

        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/95e80494ef1a7d23ee73c2d200a7ada240f0d1318161488c240a373d637f3c01-Shipping_account_block_An_Post.png" width="500px" alt="Specifying shipping account details" />

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
              <td><strong>Carrier Account Number</strong>&#42;</td>
              <td>Enter account number for An Post.</td>
            </tr>
            <tr>
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                <p>From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:</p>
                <ul>
                  <li><strong>Production</strong>: a live environment where the final version of the application is deployed and made available to the users.</li>
                  <li><strong>Sandbox</strong>: a testing environment that mimics the <strong>Production</strong> environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.</li>
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

      <ToggleListItem title="5. Save and add the shipping account" icon="fa-floppy-disk">

        <br />

        After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).
        Once done, you have now successfully added a shipping account. You can now start <Anchor label="adding the barcode range" target="_blank" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-an-post-shipping-account#/">adding the barcode range</Anchor> to it and then use it for your shipping needs.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    

    To add an An Post shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-anpost" icon="fa-code">
        Add and manage An Post shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/edit-shipping-account">
    Update or modify an existing shipping account.
  </Card>
</Cards>

<br />
