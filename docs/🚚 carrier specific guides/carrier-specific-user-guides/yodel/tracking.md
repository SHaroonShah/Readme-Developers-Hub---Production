---
title: Add YODEL tracking account
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
In SAPIENT, you can add tracking accounts for YODEL to enhance visibility, improving customer interactions, and streamlining logistics operations for YODEL.

Before adding a YODEL tracking account, you need to [send a corresponding request](ISSOnbording@Yodel.co.uk) to YODEL via email with the subject line “_Intersoft (your client name) STFP IOD tracking request_”. In the body of the email, make sure to add the following details: 

_**[Your client name] would like IOD tracking enabled for the following Yodel contract number (7 digit number). Please respond to this email with the SFTP username and password and file naming convention for IOD tracking files.**_

> 🚧 _Important_
> 
> _Prior to adding a YODEL tracking account, make sure you have completed the following prerequisites:  _ 
> 
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with YODEL. _
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with YODEL._ 
> 3. _Set up your <<glossary:tracking webhook>>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

To add a tracking account for YODEL in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3812e0d15bd2f19f64f9644a82d88a1ce95254d34f89ba7eb5de616c9fd0ff3c-Tracking_accounts_tab.png",
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


2. In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/647be94f894111181386f1ec3cdd959a85938dd4c0cd8d123d206b7db0487c8d-Add_tracking_account_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f95d0d1892b2dd558068c2cb28e4885997e9341c545c83c597ba1134c74e73ea-Add_tracking_accounts_button_YODEL.png",
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
        "https://files.readme.io/e2b0cbf7a01deef853dcf1fddd0b7bbc151c981730d577b226c9e99c6166cb26-Details_block_YODEL.png",
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
    "0-1": "From the dropdown menu, select YODEL as your carrier option.",
    "1-0": "**Shipping Account\\***",
    "1-1": "From the dropdown menu, select the <<glossary:shipping account>> for which you want to receive  tracking.  \n  \nYou can also select the **All Shipping Accounts** option to add this tracking account for all existing accounts."
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

|     Element    | Description                                                                                                                |
| :------------: | :------------------------------------------------------------------------------------------------------------------------- |
| **Username\*** | Enter the username that you have received from YODEL in response to the tracking account setup request you sent earlier.   |
| **Password\*** | Enter the password that you have received from YODEL in response to the tracking account setup request you sent earlier.   |
|  **File Path** | Enter the file path that you have received from YODEL in response to your tracking account setup request you sent earlier. |

5. After entering all the necessary information, select ![alt text](https://files.readme.io/d653c1f7e04a77a0bca6247e1bcbca03ccf933465c63ed23d2aa17b63243a632-Add_tracking_account_button_2.png).

Once done, the YODEL tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <<glossary:shipments>>.