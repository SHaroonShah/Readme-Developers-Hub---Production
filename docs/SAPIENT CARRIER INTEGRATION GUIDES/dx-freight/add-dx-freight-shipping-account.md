---
title: Add DX Freight shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Add a DX Freight shipping account in SAPIENT by selecting a <Glossary>shipping location</Glossary> and entering your account and carrier details.

In SAPIENT, you can create a DX Freight shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with DX Freight and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._

## How to add DXF shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
To add a shipping account for DX Freight in SAPIENT, perform the the steps as explained in the following procedure:
    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page" icon="bars">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account" icon="circle-plus">
        On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details" icon="clipboard-list">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/40bb3dfde408f1f6eee74c938c73d944f393452152128675900492ecb24a3e52-Account_details_block_DX_Freight.png" width="500px" alt="Entering account details" />

        <AsteridkForMandatoryElements />

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>
                Element
              </th>

              <th>
                Description
              </th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>
                **Carrier**\*
              </td>

              <td>
                From the dropdown list, select **DXF - DX Freight**.
              </td>
            </tr>

            <tr>
              <td>
                **Shipping Location**\*
              </td>

              <td>
                From the dropdown menu, select the location that you want to assign to the shipping account you are creating.

                *`Note`: Before selecting the shipping location, make sure you have[created one](https://docs.intersoftsapient.net/docs/add-a-shipping-location) beforehand.*
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details" icon="id-card">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/d0eae769c813147e1ba1ff428f31e2a84852aba1218a4858b7324d86458cd559-Shipping_account_block_DX.png" width="400px" alt="Specifying shipping account details" />

        <Callout icon="circle-info" theme="info">
          Mandatory fields in the following table are marked with an asterisk (\*).
        </Callout>

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>
                Element
              </th>

              <th>
                Description
              </th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>
                **Carrier Account Number**\*
              </td>

              <td>
                Enter the account number for DX Freight.

                The format of the account number must be compliant with the carrier you have selected. For DX Freight, the account number must be 8 characters long.

                *`Note`: If you already have an account with DX Freight that is actively being used, and if you wish to receive tracking via INTERSOFT, then you need to request DX to enable tracking and send it to INTERSOFT.*
              </td>
            </tr>

            <tr>
              <td>
                **Account Name (if different than customer)**\*
              </td>

              <td>
                Enter the name of the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Account Type**\*
              </td>

              <td>
                From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: A live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: A testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Alias**\*
              </td>

              <td>
                Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Name**\*
              </td>

              <td>
                Enter the contact name for the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Number**\*
              </td>

              <td>
                Enter the contact number for the account you are adding.
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details" icon="truck">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/3707bf4d346ea1f22c7d1d3be7bf1d030ca19d84c84998da95fc31d47eb8fc70-carrier_details_block_DX_Freight.png" width="400px" alt="Entering carrier details" />

        <AsteridkForMandatoryElements />

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>
                Element
              </th>

              <th>
                Description
              </th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>
                **Origin Service Centre (Also referred to as "Depot")**\*
              </td>

              <td>
                Enter the origin service code for identifying the correct physical location from which the <Glossary>shipments</Glossary> originate.

                *`Note`: This code may vary depending on the selected service type, for example it can be a single number or a combination of  two letters and numbers. For more information, please contact DX Freight.*
              </td>
            </tr>

            <tr>
              <td>
                **Password**\*
              </td>

              <td>
                Enter the password associated with your DX Freight account. It is essential for securing the account and ensuring that only authorized users have access to shipping details and operations.
              </td>
            </tr>

            <tr>
              <td>
                **Service Type**\*
              </td>

              <td>
                From the dropdown menu, select one the following service types that you want to use for your shipments, specifically in terms of the number of personnel involved in the delivery:

                • **1 Man**: This service type typically means that one crew member will handle the delivery. This is suitable for smaller, lighter <Glossary>items</Glossary> that one person can manage without assistance.

                • **2 Man**: This indicates that two personnel will be involved in the delivery process, which is often necessary for larger or heavier items that require additional handling or lifting.

                *`Note`: Bear in mind that you need to create separate shipping accounts for each service type that you wish to use in your shipments.*
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account" icon="floppy-disk">
        After entering all the required information, select ![alt text](https://files.readme.io/721eb0f8be0c99a924b61cbca6496517d03fcbbf235aa0c3d579c60b3131df2a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    <br />

    To add a DXF shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dxf" icon="fa-code">
        Add and manage DXF shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />

<Callout icon="book" theme="info">
  Shipping account(s) can be added and managed via API. For more information, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dxf">API References</Anchor> section.
</Callout>

### See also

* [DX Freight sign-off](https://docs.intersoftsapient.net/docs/dx-freight-sign-off)
* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)

<br />
