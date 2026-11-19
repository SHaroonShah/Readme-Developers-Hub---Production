---
title: Add Asendia shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
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

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="far fa-plus">
        <br />

        On the **Shipping Accounts** page, select ![](https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" caption="Selecting option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="far fa-address-card">
        <br />

        On the **Add Shipping Account** form, in the **ACCOUNT DETAILS** block, enter the information described below.

        <Image align="center" border={true} src="https://files.readme.io/bd4c02b7c9c557a48c13a92f58a9454ab0a5f8eb3aabdd462f6eba7147730d7d-Account_details_block_An_post.png" width="500px" caption="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :---: | :--- |
        | **Carrier**\* | From the dropdown list, select the Asendia as your carrier option. |
        | **Shipping Location**\* | rom the dropdown menu, select the location that you want to assign to the shipping account you are creating.|

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="far fa-truck">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the information described below.

        <Image align="center" border={true} src="https://files.readme.io/95e80494ef1a7d23ee73c2d200a7ada240f0d1318161488c240a373d637f3c01-Shipping_account_block_An_Post.png" width="500px" caption="Entering shipping account details
    " />

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
              <td><strong>Carrier Account Number</strong>&#42;</td>
              <td>
                Enter a ten digit account number. This must be a ten digit number. If your account number is shorter than this, then you need to add the required amount of zero's at the beginning of the number to ensure it is ten digits long.
                <br />
                The format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it is ten digit long.
              </td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                <p>From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:</p>
                <ul>
                  <li><strong>Production</strong>: a live environment where the final version of the application is deployed and made available to the users.</li>
                  <li><strong>Sandbox</strong>: a testing environment that mimics the <strong>Production</strong> environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.</li>
                </ul>
                <em><code>Note</code>: For testing purposes, you can set up a <strong>Sandbox</strong> account for Royal Mail by using a dummy account number and PLN as this data is not validated and allows you to test the integration. If you choose to switch the account to <strong>Production</strong>, then the account details are sent to the Online Business Account (OBA) team and validated. Based on this validation, the shipping account is either approved or rejected.</em>
              </td>
            </tr>
            <tr>
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Registered Email Address</strong>&#42;</td>
              <td>
                Enter the email address that was used to register the Royal Mail online business account (OBA).
                <br />
                For more information on OBA, refer to the <a href="https://docs.intersoftsapient.net/docs/oba-email-validation">Set up Royal Mail OBA account</a> section.
              </td>
            </tr>
            <tr>
              <td><strong>Registered Billing Postcode</strong></td>
              <td>
                Enter the postcode registered with Royal Mail for receiving invoices.
                <br />
                <em><code>Note</code>: If you are unsure of the postcode, use the one shown on your invoice.</em>
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

        <Image align="center" src="https://files.readme.io/0bd2bd4e7974be809da0cb97fda2d4f39e52d8177dbf53777bfa5ab3f0022b5f-image.png" width="500px" caption="Entering carrier-specific details" />

        <br />

        <AsteridkForMandatoryElements />

        <table>
          <thead>
            <tr>
              <th align="center">Element</th>
              <th align="left">Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td align="center"><strong>DHL Germany Username</strong>&#42;</td>
              <td align="left">Enter the unique identifier for the user account associated with DHL Germany.</td>
            </tr>
            <tr>
              <td align="center"><strong>DHL Germany Password</strong>&#42;</td>
              <td align="left">Enter the secure password used to authenticate the user account with DHL Germany.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account" icon="far fa-floppy-disk">
        <br />

        After entering the required information, select ![](https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png).

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add an An Post shipping account via API, refer to the following API endpoint.

    <Cards columns="2">
      <Card title="Add Account" icon="fa-code" target="_blank">
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