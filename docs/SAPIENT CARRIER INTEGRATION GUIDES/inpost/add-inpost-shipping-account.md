---
title: Add InPost shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, you can create an InPost shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

> 🚧 _Important_
>
> _Before you can set up a shipping account, be advised on the following:_
>
> * _Make sure to[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with InPost._
> * _If you wish to use both the Outbound labelled and Returns labelless services, you must create separate shipping accounts for each. This is because the credentials—**ClientId** and **Bearer token**— differs for each account._

## How to add InPost shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for InPost in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select opiton to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/8c5d5f5ff0cecf1feaa16ffc521a0feaf02bffc8c255c4ab9d967f4ad6bdf203-Account_details_block_Inpost.png" width="500px" alt="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                                                 |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **INPOST - InPost**.                                                                                         |
        | **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/aab73fec0c0be8505e9adce3450d783ae7d9f8ed4c7a9c0b9198b4682fb89679-Shipping_account_block_INPOST.png" width="500px" alt="Specifying shipping account details" />

        <br />

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

        <br />

        > 📘 *Note*
        >
        > *When creating the shipping account, InPost does not require the carrier account number. However, after creating the account, you may see the account number for your InPost shipping account in the**Account Number** column of the **Shipping Accounts** table. This number is auto-generated by the SAPIENT system and must be ignored for InPost.*

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/3a5f6be5d0522b615c12181f01d628650d3ef6d3966de74d012fce372c78a302-carrier_details_block_InPost.png" width="400px" alt="Entering carrier details" />

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
                **ClientId**\*
              </td>

              <td>
                Enter your client ID provided by InPost.
              </td>
            </tr>

            <tr>
              <td>
                **Token**\*
              </td>

              <td>
                Enter the bearer token provided by InPost.

                *`Note`: There is no authorisation/authentication API call needed to retrieve the bearer token.*
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).<br />
        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DX Express shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dx" icon="fa-code">
        Add and manage DX Express shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={3}>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off">
    Update or modify an existing shipping account.
  </Card>

  <Card title="InPost Sign-Off" icon="fa-solid fa-file-signature" href="https://docs.intersoftsapient.net/docs/inpost-sign-off">
    Complete necessary steps before using InPost to create shipments in SAPIENT.
  </Card>
</Cards>

<br />
