---
title: Add FedEx International Connect shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities
deprecated: false
hidden: true
icon: fad fa-truck-arrow-right
metadata:
  robots: index
---
In SAPIENT, with the **Add Shipping Account** functionality, you can select the desired shipping location and then add a FedEx International Connect shipping account to it

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) for FedEx International Connect._

## How to add FedEx International Connect shipping account via UI

To add a shipping account for FedEx International connect  in SAPIENT, perform the steps as explained in the following procedure.

<Tabs>
  <Tab title="Add via SAPIENT UI">
    <br />

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping accounts page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select the add shipping account button</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Accounts** page that opens, select the **Add Shipping Account** button.

        <Image align="center" border={true} src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
        <br />

        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/3d3f7869f2f26dca95da3be1dd3c6e2afe477883bca5c5c461d89250ad7073a3-image.png" width="500px" />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **FedEx International Connect**.                                               |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/53a765a066729b4aa4b2d740073f4681bc75f021b3c396fd317e9ba810a2247b-Shipping_account_block_Amazon.png" width="600px" alt="Specifying shipping account details" />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
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

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/a1f229d57e6bb784d4c1ed4b8d9353ea49753a79cdc843c0a8e4c885df8cc9f4-image.png" width="500px" />

        <AsteridkForMandatoryElements />

        <Table align={["left","left"]}>
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
                **FedEx International Connect Shipper Website URL**\*
              </td>

              <td>
                Enter the FedEx International Connect shipper website URL.

                `Note`: *This is required in the API request if shipping to the USA.*
              </td>
            </tr>

            <tr>
              <td>
                **FedEx International Connect API Key**\*
              </td>

              <td>
                Enter the API Key for the FedEx International Connect account. This API key will be sent in in your API requests.
              </td>
            </tr>
          </tbody>
        </Table>
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Save and add shipping account</strong>} icon="fa-rocket">
        <br />

        After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add via API">
    <br />

    To add a shipping account via our API, refer to the following endpoint:
<Cards columns={1}>
  <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-rm#/" icon="fa-solid fa-code">
    Complete API reference for adding shipping account
  </Card>
</Cards>
  </Tab>
</Tabs>

// Usage Example



<br />
