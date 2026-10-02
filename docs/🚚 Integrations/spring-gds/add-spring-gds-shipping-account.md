---
title: Add Spring GDS shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
icon: fad fa-square-plus
link:
  new_tab: false
metadata:
  robots: index
---
In SAPIENT, with the Add Shipping Account functionality, you can select the desired shipping location and then add a Spring GDS shipping account to it.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, make sure you have&#x20;_[_enabled the label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;for Spring GDS._
</Callout>

To add a shipping account for InPost in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.
2.
   <Image src="https://files.readme.io/5126b35b0d3d891af18e66aff39bac986726ee3d9a5a980ab09f69c3963cea61-image.png" align="center" caption="Accessing shipping accounts" border={true} />


2) On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).


<Image src="https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png" alt="Accessing option to add shipping account" align="center" caption="Selecting option to add shipping account" border={true} />


3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.


<Image src="https://files.readme.io/dc84898326356154c879fd4cf87e9428eb358a16695dc4047d41d0664a025e90-image.png" align="center" caption="Entering account details" />


<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                                                 |
| :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
|      **Carrier**\*      | From the dropdown list, select **INPOST - InPost**.                                                                                         |
| **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.


<Image src="https://files.readme.io/aab73fec0c0be8505e9adce3450d783ae7d9f8ed4c7a9c0b9198b4682fb89679-Shipping_account_block_INPOST.png" alt="Specifying shipping account details" align="center" width="500px" caption="Entering shipping account details" border={true} />


<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory fields are marked with an asterisk (\*)._
</Callout>

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Account Name (if different than customer)**\*
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Account Type**\*
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • [Production](https://docs.intersoftsapient.net/docs/sandbox-account): a live environment where the final version of the application is deployed and made available to the users.

        • [Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account): a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Alias**\*
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Contact Name**\*
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Contact Number**\*
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

<Callout icon="📘" theme="info">
  ### _Note_

  _Wh creating the shipping account, InPost does not require the carrier account number. However, after creating the account, you may see the account number for your InPost shipping account in the_**_Account Number_**_&#x20;column of the&#x20;_**_Shipping Accounts_**_&#x20;table. This number is auto-generated by the SAPIENT system and must be ignored for InPost._
</Callout>

5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.


<Image src="https://files.readme.io/a2bdd5ce64f62752e539be3e8e5db0a97cdbc787616c36f6c3130b4dfcb3a418-image.png" align="center" caption="Entering carrier-specific details" border={true} />


<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **ClientId**\*
      </td>

      <td>
        Enter your client ID provided by InPost.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Token**\*
      </td>

      <td>
        Enter the bearer token provided by InPost.

        `Note`_: There is no authorisation/authentication API call needed to retrieve the bearer token._
      </td>
    </tr>
  </tbody>
</Table>

6. After entering all the required information, select ![](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now start shipping with it.

<Callout icon="📘" theme="info">
  ### _Note_

  _Shipping account(s) can be added and managed via API. For more information, refer to the&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost">API References</Anchor>_&#x20;section._
</Callout>