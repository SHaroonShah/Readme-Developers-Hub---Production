---
title: Add Shipping Account
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
In SAPIENT, you can create a shipping account, assign your <<glossary:carrier>> credentials to it, and then link them to the relevant <<glossary:shipping location>>(s).  

> 📘 _Note_
> 
> _Users with the **Admin** role permissions can create unlimited shipping accounts for their customers._

To create a shipping account in SAPIENT, follow the instructions as explained in the following procedure.

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


2. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/0a2190f702c512528e9b264765a05e8b507cecbb379fd3fe390767ed8518382a-add_shipping_account_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png",
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


3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following tables.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png",
        null,
        "Entering account details"
      ],
      "align": "center",
      "border": true,
      "caption": "Entering account details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                                |
| :---------------------: | :------------------------------------------------------------------------------------------------------------------------- |
|      **Carrier\***      | From the dropdown list, select the carrier for which you want to add a shipping account.                                   |
| **Shipping Location\*** | From the dropdown menu, select the location that you want to assign to the <<glossary:shipping account>> you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png",
        "",
        "Specifying shipping account details"
      ],
      "align": "center",
      "sizing": "400px",
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
    "0-1": "Enter the carrier account number.  \n  \nThe format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it lies within the standard character length range for that carrier.",
    "1-0": "**Account Type\\***",
    "1-1": "From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:  \n  \n• **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.  \n  \n• **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.",
    "2-0": "**Account Name (if different than customer)\\***",
    "2-1": "Enter the account name. ",
    "3-0": "**Registered Email Address\\***",
    "3-1": "Enter the email address that was used to register the account for the carrier you selected.",
    "4-0": "**Registered Billing Postcode**",
    "4-1": "Enter the postcode registered with the carrier for receiving invoices.",
    "5-0": "**Alias\\***",
    "5-1": "Enter a custom name which can be used in the API request instead of using the shipping location ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.",
    "6-0": "**Contact Name\\***",
    "6-1": "Enter the contact name for the account you are adding.",
    "7-0": "**Contact Number\\***",
    "7-1": "Enter the contact number for the account you are adding."
  },
  "cols": 2,
  "rows": 8,
  "align": [
    "center",
    "left"
  ]
}
[/block]


5. In the **CARRIER DETAILS** block, the fields you see are carrier-specific and vary for each carrier. To get more information on how to fill the fields in this block, refer to the [carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides) section.
6. After entering all the required information, select ![alt text](https://files.readme.io/c8e36ac323cf6d3859bfa7081ee7ab63495ded4fd04cdb97aa685e06071cf4b4-add_shipping_account_button_2.png).

 Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

> 📘 _Note_
> 
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._