---
title: Add UPS tracking account
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
In SAPIENT, you can add tracking accounts for UPS to enhance visibility, improving customer interactions, and streamlining logistics operations for UPS.

> 🚧 *Important*
>
> *Prior to adding a UPS tracking account, make sure you have completed the following prerequisites:* 
>
> 1. *Enabled the[label integration](https://docs.intersoftsapient.net/docs/integration-activation) with UPS.*
> 2. *Enabled the[tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with UPS.* 
> 3. *Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account.*

To add a tracking account for UPS in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

<Image alt="Accessing tracking accounts" align="center" border={true} src="https://files.readme.io/c3f6098979696b25cbdbe26921658742edef4520e983ae8c70cbe6f689e4aadf-Tracking_accounts_tab.png">
  Accessing tracking accounts
</Image>

2. In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/63f1badb667ff6379f323bdc6485e8a519eb46938b0dcd4b98e384686ebb68e0-Add_tracking_account_button.png).

<Image alt="Accessing option to add tracking account" align="center" border={true} src="https://files.readme.io/c2f04a8e6b4e985e203082e192cfe4d35f0702aa38fa593bb2440e490295dd3a-Add_tracking_account_button_UPS.png">
  Accessing option to add tracking account
</Image>

3. On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

<Image alt="Adding tracking account" align="center" width="500px" border={true} src="https://files.readme.io/d5239464ffac95ad4b5081802a5b002a3e966e94ab27e760cf7ba3d2eeecaf56-Details_block_UPS.png">
  Adding tracking account
</Image>

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                                      |
| :--------------------: | :--------------------------------------------------------------------------------------------------------------- |
|      **Carrier\***     | From the dropdown menu, select UPS as your carrier option.                                                       |
| **Shipping Account\*** | From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking. |

4. After entering all the necessary information, select ![alt text](https://files.readme.io/41bf635f2c82bf95197e5a2f62939d396ead6033e48a985a30965d84a5be57b8-Add_tracking_account_button_2.png).

Once done, the UPS tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
