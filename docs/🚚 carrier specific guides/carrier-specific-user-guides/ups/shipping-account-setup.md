---
title: Add UPS shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a shipping account with UPS, assign your UPS credentials to it, and then link it to the relevant <Glossary>shipping location</Glossary>(s).

> 🚧 *Important*
>
> *Before you can set up a shipping account, make sure you have[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with UPS.*

To add a shipping account for UPS in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**. 

<Image alt="Accessing shipping accounts" align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png">
  Accessing shipping accounts
</Image>

3. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/a68fed3fbbb1668dedfcf9e0a5bd246f3f1dfa92bb6c7a47c175ad8df700e827-add_shipping_account_button.png).

<Image alt="Accessing option to add shipping account" align="center" border={true} src="https://files.readme.io/e0071b9f348522956cf0d9db5802f5bef56a11c5d3ff90f8a6bbedbc3c48d560-Add_shipping_account_button_UPS.png">
  Selecting option to add shipping account
</Image>

4. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image alt="Entering account details" align="center" width="500px" border={true} src="https://files.readme.io/a1e3a2edb2b84155855b5d3ef2e3f44e2884976af6a88883e53504fbcb2e5af2-Account_details_block_UPS.png">
  Entering account details
</Image>

<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                   |
| :---------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier\***      | From the dropdown list, select **UPS**.                                                                       |
| **Shipping Location\*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

5. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image alt="Specifying shipping account details" align="center" width="400px" border={true} src="https://files.readme.io/ba28fb8f7a5840840e921e8649cf481a3c115804447f269786068d434d15fbcb-Shipping_account_block_UPS.png">
  Specifying shipping account details
</Image>

> 💡 *Tip*
>
> *In the following table, the mandatory fields are marked with an asterisk (\*).*

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Carrier Account Number\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the account number for UPS.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Account Name (if different than customer)\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Account Type\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:  

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.  

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Alias\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Contact Name\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Contact Number\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

6. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image alt="Entering carrier details" align="center" width="400px" border={true} src="https://files.readme.io/a3b23bd3c50a8e648377a238d6eefe16f86441b03cc9c33a7bd6a7321b8640fe-carrier_details_block_UPS.png">
  Entering carrier details
</Image>

<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **UPS Client Id\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your UPS client ID.  

        `Note`: In order to obtain your client ID, you need to create an application. This application is linked to your shipper account(s) and email address that are associated with your ups.com ID.  For a step by step guide on how to get these credentials, refer to the [Getting Started with UPS APIs](https://developer.ups.com/get-started?loc=en_US\&utm_source=hs_email\&utm_medium=email&_hsenc=p2ANqtz-8n0kt_beo2J5QHe3SljjztyPcwEo3zauJzWPnJINftBYbljxxRD5Wv334sxXTuPf_-cyWE) user guide.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **UPS Client Secret\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your UPS client secret.  

        `Note`: In order to obtain your client secret, you need to create an application. This application is linked to your shipper accounts(s) and email address that are associated with your ups.com ID.  For a step by step guide on how to get these credentials, refer to the [Getting Started with UPS APIs](https://developer.ups.com/get-started?loc=en_US\&utm_source=hs_email\&utm_medium=email&_hsenc=p2ANqtz-8n0kt_beo2J5QHe3SljjztyPcwEo3zauJzWPnJINftBYbljxxRD5Wv334sxXTuPf_-cyWE) user guide.
      </td>
    </tr>
  </tbody>
</Table>

7. After entering all the required information, select ![alt text](https://files.readme.io/7bacd208cbc1e3036e95df7c94e4b08f4f731910cf76b88ddd1eb137177b4018-add_shipping_account_button_2.png).

 Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

***

## Account approval

Once you have created the UPS shipping account, the account needs to be approved before you start using it to ship with UPS.

To get your shipping account approved, consider the following:  

1. If the account type you have created is **Production**, you will receive a confirmation email. 
2. Initially, the account status is set to **'Disabled'** until the account has been approved by the UPS's IT integration team. This can typically take 2-5 working days. 
3. Once the account has been approved, the status of your shipping account is change to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-evri) API. 
4. If the account cannot be approved, we will contact you and advise accordingly. 

> 📘 *Note*
>
> *Shipping account(s) can be added and managed via API. For more information, refer to the[API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section.*

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)
