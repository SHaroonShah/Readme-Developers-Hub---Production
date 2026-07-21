---
title: Add DPD Ireland shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, with the **Add Shipping Account** functionality, you can select the desired shipping location and then add a DPD Ireland shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have enabled the <Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for DPD Ireland._
</Callout>

## How to add DPD Ireland shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for DPD Ireland in SAPIENT, perform the steps in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">

        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" caption="Accessing shipping accounts" src="https://files.readme.io/3d2349061f0415b118f4ffc1d5d1f0722422302161528022cbc28634eb90514f-image.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">

        <br />

        On the **Shipping Accounts** page that opens, select <Image src="https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png" caption="Add shipping account button" />.

        <Image align="center" caption="Selecting option to add shipping account" src="https://files.readme.io/a42649a2e896b24618507db2db02d7f7347225eabc56e04b4f79bcefea7c8ea8-image.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">

        <br />

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information described in the following table.

        <Image align="center" width="550px" src="https://files.readme.io/86645219f87b869aff196c809ef6249918aa0e14533c668a9ac0b8be1f007cd9-image.png" />

        <br />

        <AsteridkForMandatoryElements />

        <table>
          <thead>
            <tr>
              <th align="left">Element</th>
              <th align="left">Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td align="left"><strong>Carrier</strong>&#42;</td>
              <td align="left">From the dropdown list, select <strong>DPDIE - DPD Ireland</strong>.</td>
            </tr>
            <tr>
              <td align="left"><strong>Shipping Location</strong>&#42;</td>
              <td align="left">From the dropdown menu, select the location that you want to assign to the shipping account you are creating.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">

        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information described in the following table.

        <Image align="center" width="500px" src="https://files.readme.io/c18989ccd749f6910c3f73b85cbf2bcca73358ef809018f03cfb226f78a6b82e-image.png" />

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
              <td align="center"><strong>Carrier Account Number</strong>&#42;</td>
              <td align="left">Enter the carrier account number assigned to you by DPD Ireland.</td>
            </tr>
            <tr>
              <td align="center"><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td align="left">Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td align="center"><strong>Account Type</strong>&#42;</td>
              <td align="left">From the dropdown menu, select the account type for the shipping account you are adding:<br /><br /><ul><li><a href="https://docs.intersoftsapient.net/docs/sandbox-account"><strong>Production</strong></a>: a live environment where the final version of the application is deployed and made available to users.</li><li><a href="https://docs.intersoftsapient.net/docs/sandbox-account"><strong>Sandbox</strong></a>: a testing environment that mimics the <strong>Production</strong> environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.</li></ul></td>
            </tr>
            <tr>
              <td align="center"><strong>Alias</strong>&#42;</td>
              <td align="left">Enter a custom name that you can use in API requests instead of the shipping account ID. Use a memorable name that is available for reference purposes.</td>
            </tr>
            <tr>
              <td align="center"><strong>Contact Name</strong>&#42;</td>
              <td align="left">Enter the contact name for the account you are adding.</td>
            </tr>
            <tr>
              <td align="center"><strong>Contact Number</strong>&#42;</td>
              <td align="left">Enter the contact number for the account you are adding.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details">

        <br />

        In the **CARRIER DETAILS** block, enter the necessary information described in the following table.

        <Image align="center" width="500px" src="https://files.readme.io/d4b4a30602ad21751b1cd1860976f17f00995d772dcbc15e817dde6c4188a483-image.png" />

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
              <td align="center"><strong>Username</strong>&#42;</td>
              <td align="left">Enter the username provided by DPD Ireland. SAPIENT uses it in API requests to authenticate the shipping account.</td>
            </tr>
            <tr>
              <td align="center"><strong>Password</strong>&#42;</td>
              <td align="left">Enter the password associated with the DPD Ireland account. SAPIENT uses it with the username for API authentication.</td>
            </tr>
            <tr>
              <td align="center"><strong>Basic Token</strong>&#42;</td>
              <td align="left">Enter the secure authentication token provided by DPD Ireland. This token is sent in the request header to support API authorisation; treat and store it as a password.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">

        <br />

        After entering all the required information, select <Image src="https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png"/>.

        Once done, you have successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add and manage a shipping account via API, refer to the following API reference.

    <Cards>
      <Card title="API References" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dhlde" icon="fa-code">
        Add and manage shipping accounts via API.
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
