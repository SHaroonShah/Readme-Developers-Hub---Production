---
title: Add YODEL shipping account
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
In SAPIENT, with the Add Shipping Account functionality, you can select the desired shipping location and then add a YODEL shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have enabled the <Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for YODEL and have already <Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location">created a shipping location</Anchor>._
</Callout>

## How to add YODEL shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for YODEL in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

        <Image align="center" src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" caption="Selecting option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/c430911306cfc97f8609b300891198244b5504b1eb732e5cb8199dec132659eb-Account_details_block_YODEL.png" width="500px" caption="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        | Element                 | Description                                                                                                                                 |
        | :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
        | **Carrier**\*           | From the dropdown list, select **YODEL - Yodel**.                                                                                           |
        | **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/4668084ea31679c03a9b0cee35f97a98dff1a6a9b196155c7fb39b9e91c7b66e-Shipping_account_block_YODEL.png" width="500px" caption="Entering shipping account details" />

        <br />

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
                **Carrier Account Number**\*
              </td>

              <td>
                Enter the nine digit account number for YODEL.
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

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Alias**\*
              </td>

              <td>
                Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
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

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/a2d5436c5b557ca7ba52fbd8239764e70cb7b9449239eceea0d5d0796ec7be3b-carrier_details_block_YODEL.png" width="400px" caption="Entering carrier-specific details" />

        <br />

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
                **Contract Number**\*
              </td>

              <td>
                Enter your seven digit YODEL contract number.
              </td>
            </tr>

            <tr>
              <td>
                **Schedule Number**\*
              </td>

              <td>
                Enter your four digit YODEL schedule number.
              </td>
            </tr>

            <tr>
              <td>
                **Meter Number**\*
              </td>

              <td>
                Enter your five digit meter number.

                This number is used to create the unique YODEL barcode range.

                *`Note:`The meter number must be unique and cannot be duplicated across shipping accounts.*
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a YODEL shipping account via API, refer to the following API endpoint.

    <Cards columns="2">
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-yodel" icon="fa-code" target="_blank">
        Add and manage YODEL shipping account via API.
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

  <Card title="Add barcode range to shipping account" href="https://docs.intersoftsapient.net/docs/barcode-range-setup-1" icon="fa-solid fa-barcode" target="_blank">
    Add barcode ranges to facilitate efficient tracking and management of shipments.
  </Card>
</Cards>
