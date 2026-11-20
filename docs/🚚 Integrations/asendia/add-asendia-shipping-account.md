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

  _Before you can set up a shipping account, make sure you have&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">_enable the label integration_</Anchor>_&#x20;with Asendia and and already&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location">_created a shipping location_</Anchor>_._
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

        
    <Image src="https://files.readme.io/95b6bb934de15922a586816dd1975e4c520f4fd6623a863cfa5f77e4ed7bdf04-image.png" align="center" caption="Entering account details" border={true} />


        <br />

        <AsteridkForMandatoryElements />

        | Element | Description |
        | :---: | :--- |
        | **Carrier**\* | From the dropdown list, select the Asendia as your carrier option. |
        | **Shipping Location**\* | From the dropdown list, select the location that you want to assign to the shipping account you are creating.|

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="far fa-truck">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the information described below.

        
    <Image src="https://files.readme.io/c31cdd42822de25b509117e4a79c2c315315f0e9dcf4077753816581a429f382-image.png" align="center" caption="Entering shipping account details" border={true} />


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
                Enter the 10-digit CRMID number assigned by Asendia.

    <em><code>Note:</code> If you are unsure of this number, contact your Asendia account manager.<em>
              </td>
            </tr>
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

        
    <Image src="https://files.readme.io/e2b20cf5cd539a1e2674ba8998e2517b83bafdb080cc566778e6d4161704679a-image.png" align="center" caption="Entering carrier-specific details" border={true} />


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
              <td align="center"><strong>API Key</strong>&#42;</td>
              <td align="left">Enter the API key for the user account associated with Asendia.</td>
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