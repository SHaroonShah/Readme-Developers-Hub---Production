---
title: Add Royal Mail shipping account
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
In SAPIENT, you can create a shipping account with Royal Mail, assign your Royal Mail credentials to it, and then link it to the relevant <<glossary:shipping location>>(s).  

> 🚧 _Important_
> 
> _Before you can set up a shipping account, you must ensure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with Royal Mail._

To add a shipping account for Royal Mail in SAPIENT, follow the instructions as explained in the following procedure.

1. Log in to the SAPIENT platform using your credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa5d0ced6ed38b419fa15c57f5b03fdddf6284adfcc85b48370c67d1aa07c5f8-Sapient_Login_window.png",
        "",
        "Logging into SAPIENT"
      ],
      "align": "center",
      "sizing": "500px",
      "border": true,
      "caption": "Logging into SAPIENT"
    }
  ]
}
[/block]


2. On the **Home** page that opens, in the left navigation panel, select **Shipping Accounts**. 

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


3. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/44690bc0342682d80d45da0ca9e41920f4a8e30430a7279053ef6348e2900569-add_shipping_account_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a8c9af67fce1cfe9d27b55871687460e467417da0f236b1fa0a7a622241a67d-RM_create_shiipping_accounts_option.png",
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


4. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

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

|         Element         | Description                                                                                                   |
| :---------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier\***      | From the dropdown list, select **RM - Royal Mail**.                                                           |
| **Shipping Location\*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

5. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

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
    "0-1": "Enter a ten digit account number. This must be a ten digit number. If your account number is shorter than this, then you need to add the required amount of zero's at the beginning of the number to ensure it is ten digits long.  \n  \nThe format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it is ten digit long.",
    "1-0": "**Account Type\\***",
    "1-1": "From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:  \n  \n• **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.  \n  \n• **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.",
    "2-0": "**Account Name (if different than customer)\\***",
    "2-1": "Enter the name of the account you are adding. ",
    "3-0": "**Registered Email Address\\***",
    "3-1": "Enter the email address that was used to register the Royal Mail online business account (OBA).  \n  \nFor more information on OBA, refer to the [Set up Royal Mail OBA account](https://docs.intersoftsapient.net/docs/oba-email-validation) section.",
    "4-0": "**Registered Billing Postcode**",
    "4-1": " Enter the postcode registered with Royal Mail for receiving invoices.",
    "5-0": "**Alias\\***",
    "5-1": "Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.",
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


6. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ca47335dbea534cb7d1b4ddce82c5eef9de68c4e17ac2c7169d6b82f3738835-carrier_details_block.png",
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
    "0-0": "**Posting Location Code\\***",
    "0-1": "This is a Royal Mail specific code given for each location you are despatching shipments from.  \n  \nThis must be a 10 digit number that always starts with 9000. For example, 9000257150.",
    "1-0": "**Receiving Hub Code\\***",
    "1-1": "Enter the code allocated by Royal Mail for the receiving Hub to where your goods will be taken.  \n  \nThe **Receiving Hub Code** is automatically populated based on the postcode of the shipping location to which you are linking this account.",
    "2-0": "**OBA Access Code**",
    "2-1": "This field is autopopulated by INTERSOFT and is something we communicate directly with the carrier after the shipping account has been added."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "center",
    "left"
  ]
}
[/block]


7. After entering all the required information, select ![alt text](https://files.readme.io/db03c9a2b7ee816f42db617829469dce01bbdfd35aca00ace480fd78db31aa11-add_shipping_account_button_2.png).

 Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

***

## Account approval

Once you have created the Royal Mail shipping account, the account needs to be approved before you start using it to ship with Royal Mail.

To get your shipping account approved, consider the following:  

1. If the <<glossary:account type>> you have created is **Production**, you will receive a confirmation email. 
2. Initially, the account status is set to **'Disabled'** until the account has been approved by the Royal Mail OBA team. This can typically take 2-5 working days. 
3. Once the account has been approved, the status of your shipping account is changed to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-rm-shippingaccountid) API. 
4. If the account cannot be approved, we will contact you and advise accordingly. 

> 📘 _Note_
> 
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._

To view a step-by-step process on how to add a Royal Mail shipping account with a new shipping location, refer to the following API recipe:

[block:tutorial-tile]
{
  "backgroundColor": "#8d8f91",
  "emoji": "🏦",
  "id": "64353537ec43f4006b97047f",
  "link": "https://docs.intersoftsapient.net/v4.02/recipes/create-a-royal-mail-shipping-account-with-a-new-shipping-location",
  "slug": "create-a-royal-mail-shipping-account-with-a-new-shipping-location",
  "title": "Create a Royal Mail shipping account with a new shipping location"
}
[/block]


### See also

- [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)