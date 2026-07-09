---
title: Add DHL Express shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
metadata:
  robots: index
---
In SAPIENT, with the **Add Shipping Account** functionality, you can select the desired shipping location and then add a DHL Express shipping account to it.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have enabled the <Anchor label="label integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for DHL Express._

## How to add DHL Express shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for DHL Express in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" src="https://files.readme.io/3d2349061f0415b118f4ffc1d5d1f0722422302161528022cbc28634eb90514f-image.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png).

        <Image align="center" src="https://files.readme.io/a42649a2e896b24618507db2db02d7f7347225eabc56e04b4f79bcefea7c8ea8-image.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/d714b6b8967ed58d6d5afb7ddb6c42cff2c139fee07f29a7e4d62cde604fc491-image.png" width="500px" />

        <br />

        <AsteridkForMandatoryElements />

        | Element                 | Description                                                                                                   |
        | :---------------------- | :------------------------------------------------------------------------------------------------------------ |
        | **Carrier**\*           | From the dropdown list, select DHLEXPRESS -  DHL Express.                                                     |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/83810f18ee92f48d62b60191f940531365a413ee892f5fc77f3fd76772e24e87-image.png" width="400px" />

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
              <td>Enter the carrier account number assigned to you by DHL Express.</td>
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

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/d8c8146f35ea4e12d7eb755dbd2d0d3bb37731978b8bdf385a478a1cf5c36445-image.png" width="500px" />

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
              <td>Enter the API key for the user account associated with DHL Express.</td>
            </tr>
            <tr>
              <td><strong>API Secret</strong>&#42;</td>
              <td>Enter the API secret used to authenticate the user account with DHL Express.</td>
            </tr>
            <tr>
              <td><strong>Archive Labels</strong></td>
              <td>
                Turn on the toggle if you wish to include the DHL archived labels in the manifest.
                <br />
                <br />
                Enabling this toggle saves DHL waybill documents from the create shipment response in the database and includes them in the manifest PDF when shipments are manifested.
                <br />
                <br />
                <em><code>Note</code>: The manifests can be downloaded from the SAPIENT’s <a href="https://docs.intersoftsapient.net/docs/manifest-history">View manifest history page</a>.</em>
              </td>
            </tr>
            <tr>
              <td colspan="2">
                <strong>Enable Paperless Trade (PLT)</strong>
                <br />
                <br />
                Turn on the toggle if you want to submit the customs documents electronically. If this toggle is enabled, then you must specify one the following options:
              </td>
            </tr>
            <tr>
              <td><strong>Allow DHL to generate commercial invoices on your behalf</strong></td>
              <td>Select this option for DHL to create and send the invoice electronically to the customs agency.</td>
            </tr>
            <tr>
              <td><strong>Use SAPIENT-generated invoices</strong></td>
              <td>Select this option to have SAPIENT generate the invoices from shipment data and send them to DHL.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DHL Express shipping account via API, refer to the API References section.

    <Cards>
      <Card title="Add Account" href="" icon="fa-code">
        Add and manage DHL Express shipping account via API.
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