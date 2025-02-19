---
title: Add EVRi tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add tracking accounts for EVRi to enhance visibility, improving customer interactions, and streamlining logistics operations for EVRi.

Before adding an EVRi tracking account, you need to [send a corresponding request to EVRi](mailto:evriclientdesk@evri.com) via email with your EVRi client account manager cc'd in your request. In the email, make sure to add the following information:

- **Client ID**
- **Client name**
- **Schedule for receiving tracking files**

 It can take up to 5 working days for EVRi to set up the tracking and provide the relevant credentials.

> 🚧 _Important_
> 
> _Prior to adding an EVRi tracking account, make sure you have completed the following prerequisites:  _ 
> 
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with EVRi. _
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with EVRi._ 
> 3. _Set up your <<glossary:tracking webhook>>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

To add a tracking account for EVRi in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0b0bf418cd10c99ea179b79f676a9185f00ad99670333f70f1848e77f0ee2fef-Tracking_accounts_tab.png",
        "",
        "Accessing tracking accounts"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing tracking accounts"
    }
  ]
}
[/block]


2. In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/1797ee1f92c9e2a16f6b55d7a84e3ef14111e4ef4a7b3e13ff1acb538c1447e8-Add_tracking_account_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/faca47a22b3d4de7d74e54c6ea663a5156625b787a81a5c7568d2ef0688da840-Add_tracking_account_button_EVRi.png",
        "",
        "Accessing option to add tracking account"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing option to add tracking account"
    }
  ]
}
[/block]


3. On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7659a1bf5fc38bc305bdb0fcca75fc3dd4d965efb34cb7a038bbd1ca34235cde-Details_block_EVRi.png",
        "",
        "Adding tracking account"
      ],
      "align": "center",
      "sizing": "500px",
      "border": true,
      "caption": "Adding tracking account"
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
    "0-0": "**Carrier\\***",
    "0-1": "From the dropdown menu, select EVRi as your carrier option.",
    "1-0": "**Shipping Account\\***",
    "1-1": "From the dropdown menu, select the <<glossary:shipping account>> for which you want to receive tracking.  \n  \nYou can also select the **All Shipping Accounts** option to add this tracking account for all existing accounts."
  },
  "cols": 2,
  "rows": 2,
  "align": [
    "center",
    "left"
  ]
}
[/block]


4. In the **SFTP DETAILS** block, enter the necessary information as explained in the following table:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b2437869c8baecd092365fb5631a2dc0e31e07454c824245442ab67bc10ec14c-SFTP_details_block_EVRi.png",
        "",
        ""
      ],
      "align": "center",
      "sizing": "500px"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

|     Element    | Description                                                                                                               |
| :------------: | :------------------------------------------------------------------------------------------------------------------------ |
| **Username\*** | Enter the username that you have received from EVRi in response to the tracking account setup request you sent earlier.   |
| **Password\*** | Enter the password that you have received from EVRi in response to the tracking account setup request you sent earlier.   |
|  **File Path** | Enter the file path that you have received from EVRi in response to your tracking account setup request you sent earlier. |

5. After entering all the necessary information, select ![alt text](https://files.readme.io/f713760b5bde9e21d187c9b978502b434343e34f9f3db55afa5b565d35d478cd-Add_tracking_account_button_2.png).

Once done, the EVRi tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <<glossary:shipments>>.