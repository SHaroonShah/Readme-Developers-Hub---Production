---
title: Add YODEL shipping account
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
In SAPIENT, you can create a shipping account with YODEL, assign your YODEL credentials to it, and then link it to the relevant <<glossary:shipping location>>(s).

> 🚧 _IMPORTANT_
> 
> _Before you can set up a shipping account, make sure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with YODEL._

To add a shipping account for YODEL in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png",
        "",
        "Accessing shipping accounts"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing shipping accounts"
    }
  ]
}
[/block]


2. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/e27a112101fea1d20bb870a5c570ce3cb3889d2c514dd5bc0920c2ea630f9943-add_shipping_account_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f21da8d1e1c679c2ed31d67bfc7551e5c9477f2f22b16c279aed71ab9688809-Add_shipping_account_button_YODEL.png",
        "",
        "Accessing option to add shipping account"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting option to add shipping account"
    }
  ]
}
[/block]


3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c430911306cfc97f8609b300891198244b5504b1eb732e5cb8199dec132659eb-Account_details_block_YODEL.png",
        null,
        "Entering account details"
      ],
      "align": "center",
      "sizing": "500px",
      "border": true,
      "caption": "Entering account details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                                         |
| :---------------------: | :---------------------------------------------------------------------------------------------------------------------------------- |
|      **Carrier\***      | From the dropdown list, select **YODEL - Yodel**.                                                                                   |
| **Shipping Location\*** | From the dropdown menu, select the <<glossary:shipping location>> that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4668084ea31679c03a9b0cee35f97a98dff1a6a9b196155c7fb39b9e91c7b66e-Shipping_account_block_YODEL.png",
        "",
        "Specifying shipping account details"
      ],
      "align": "center",
      "sizing": "500px",
      "border": true,
      "caption": "Specifying shipping account details"
    }
  ]
}
[/block]


> 💡 _Tip_
> 
> _In the following table, the mandatory fields are marked with an asterisk (\*)._

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "0-0": "**Carrier Account Number\\***",
    "0-1": "Enter the nine digit account number for YODEL.",
    "1-0": "**Account Name (if different than customer)\\***",
    "1-1": "Enter the name of the account you are adding.",
    "2-0": "**Account Type\\***",
    "2-1": "From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:  \n  \n• **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.  \n  \n• **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.",
    "3-0": "**Alias\\***",
    "3-1": "Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.",
    "4-0": "**Contact Name\\***",
    "4-1": "Enter the contact name for the account you are adding.",
    "5-0": "**Contact Number\\***",
    "5-1": "Enter the contact number for the account you are adding."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "center",
    "left"
  ]
}
[/block]


5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a2d5436c5b557ca7ba52fbd8239764e70cb7b9449239eceea0d5d0796ec7be3b-carrier_details_block_YODEL.png",
        "",
        "Entering carrier details"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Entering carrier details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "0-0": "Contract Number\\*",
    "0-1": "Enter your seven digit YODEL contract number.",
    "1-0": "Schedule Number\\*",
    "1-1": "Enter your four digit YODEL schedule number",
    "2-0": "Meter Number",
    "2-1": "Enter your five digit meter number.  \n  \nThis number is used to create the unique YODEL barcode range."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "center",
    "left"
  ]
}
[/block]


6. After entering all the required information, select ![alt text](https://files.readme.io/4d8fd2c9a6fad152f41e65d82274b94a6d3a8978f69bb88fbe74ba2d54138fe8-add_shipping_account_button_2.png).

 Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

***

## Account approval

Once you have created the YODEL shipping account, the account needs to be approved before you start using it to ship with YODEL.

To get your shipping account approved, consider the following:  

1. If the account type you have created is **Production**, you will receive a confirmation email. 
2. Initially, the account status is set to **'Disabled'** until the account has been approved by the YODEL's IT integration team. This can typically take 2-5 working days. 
3. Once the account has been approved, the status of your shipping account is change to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://api.test.intersoftsapient.net/docs/v4-YODEL/api/index.html#tag/Shipping-Accounts/paths/~1v4~1shippingAccounts~1yodel~1%7BshippingAccountId%7D/get) API. 
4. If the account cannot be approved, we will contact you and advise accordingly. 

> 📘 _Note_
> 
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._

### See also

- [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)