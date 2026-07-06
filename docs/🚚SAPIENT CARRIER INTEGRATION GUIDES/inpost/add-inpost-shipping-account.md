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

To add a shipping account for InPost in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/8c5d5f5ff0cecf1feaa16ffc521a0feaf02bffc8c255c4ab9d967f4ad6bdf203-Account_details_block_Inpost.png" width="500px" />

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                                                                 |
| :--------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
|      **Carrier***      | From the dropdown list, select **INPOST - InPost**.                                                                                         |
| **Shipping Location*** | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Entering shipping account details" src="https://files.readme.io/aab73fec0c0be8505e9adce3450d783ae7d9f8ed4c7a9c0b9198b4682fb89679-Shipping_account_block_INPOST.png" width="500px" />

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory fields are marked with an asterisk (*)._
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
        **Account Name (if different than customer)***
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Alias***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 _Note_
>
> _Wh creating the shipping account, InPost does not require the carrier account number. However, after creating the account, you may see the account number for your InPost shipping account in the**Account Number** column of the **Shipping Accounts** table. This number is auto-generated by the SAPIENT system and must be ignored for InPost._

5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/3a5f6be5d0522b615c12181f01d628650d3ef6d3966de74d012fce372c78a302-carrier_details_block_InPost.png" width="400px" />

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
        **ClientId***
      </td>

      <td>
        Enter your client ID provided by InPost.
      </td>
    </tr>

    <tr>
      <td>
        **Token***
      </td>

      <td>
        Enter the bearer token provided by InPost.

        _`Note`: There is no authorisation/authentication API call needed to retrieve the bearer token._
      </td>
    </tr>
  </tbody>
</Table>

6. After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now start shipping with it.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost">API References</Anchor> section._

***

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)
