---
title: Add Asendia shipping account
deprecated: false
hidden: true
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, you can create an Asendia shipping account by selecting your desired shipping location, entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you set up a shipping account,&#x20;_[_enable the label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with Asendia and&#x20;_[_create a shipping location_](https://docs.intersoftsapient.net/docs/add-a-shipping-location)_._
</Callout>

## How to add Asendia shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add an Asendia shipping account via the SAPIENT user interface (UI), perform the steps as explained in the following procedure:

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page" icon="far fa-arrow-pointer">
        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Shipping Accounts option in the navigation panel" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="far fa-plus">
        <br />

        On the **Shipping Accounts** page, select <Image src="https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png" caption="Add shipping account button" />.

        <Image align="center" border={true} src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" caption="Option to add a shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="far fa-address-card">
        <br />

        On the **Add Shipping Account** form, in the **ACCOUNT DETAILS** block, enter the information described below.

        <Image align="center" border={true} src="https://files.readme.io/bd4c02b7c9c557a48c13a92f58a9454ab0a5f8eb3aabdd462f6eba7147730d7d-Account_details_block_An_post.png" width="500px" caption="Account details — source image awaiting replacement" />

        <br />

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :---: | :--- |
        | **Carrier**\* | Select the Asendia carrier option. |
        | **Shipping Location**\* | Select the shipping location to assign to the account. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="far fa-truck">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the information described below.

        <Image align="center" border={true} src="https://files.readme.io/95e80494ef1a7d23ee73c2d200a7ada240f0d1318161488c240a373d637f3c01-Shipping_account_block_An_Post.png" width="500px" caption="Shipping account details — source image awaiting replacement" />

        <br />

        <AsteridkForMandatoryElements />

        <table>
          <thead>
            <tr>
              <th style={{ backgroundColor: '#444444', color: '#ffffff', textAlign: 'center' }}>Element</th>
              <th style={{ backgroundColor: '#444444', color: '#ffffff', textAlign: 'center' }}>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Carrier Account Number</strong>&#42;</td>
              <td>Enter your Asendia account number.</td>
            </tr>
            <tr>
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                <p>Select the account type:</p>
                <ul>
                  <li><strong>Production</strong>: the live environment used for shipping.</li>
                  <li><strong>Sandbox</strong>: an isolated environment used for development and testing.</li>
                </ul>
              </td>
            </tr>
            <tr>
              <td><strong>Alias</strong>&#42;</td>
              <td>Enter a memorable custom name to use in an application programming interface (API) request instead of the shipping account identifier.</td>
            </tr>
            <tr>
              <td><strong>Contact Name</strong>&#42;</td>
              <td>Enter the contact name for the account.</td>
            </tr>
            <tr>
              <td><strong>Contact Number</strong>&#42;</td>
              <td>Enter the contact number for the account.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Save and add the shipping account" icon="far fa-floppy-disk">
        <br />

        After entering the required information, select <Image src="https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png" caption="Add shipping account button" /> to add the shipping account.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add an An Post shipping account via API, refer to the following API endpoint.

    <Cards columns="2">
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-anpost" icon="fa-code" target="_blank">
        Add and manage Asendia shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="far fa-pen-to-square" target="_blank">
    Update or modify an existing shipping account.
  </Card>
</Cards>