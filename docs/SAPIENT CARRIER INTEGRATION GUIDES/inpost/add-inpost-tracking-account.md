---
title: Add InPost tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: false
icon: fad fa-calendar-circle-plus
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for InPost to enhance visibility, improving customer interactions, and streamlining logistics operations for InPost.

> 🚧 _Important_
>
> _Prior to adding InPost tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the[label integration](https://docs.intersoftsapient.net/docs/integration-activation) with InPost._
> 2. _Enabled the[tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with InPost._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

## How to add InPost tracking account

To add a tracking account for InPost in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Navigate to the Tracking Accounts tab">
    In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/c3f6098979696b25cbdbe26921658742edef4520e983ae8c70cbe6f689e4aadf-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />
***
  </ToggleListItem>
<br />
  <ToggleListItem title="2. Select option to add tracking account">
    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/63f1badb667ff6379f323bdc6485e8a519eb46938b0dcd4b98e384686ebb68e0-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/c2f04a8e6b4e985e203082e192cfe4d35f0702aa38fa593bb2440e490295dd3a-Add_tracking_account_button_UPS.png" alt="Accessing option to add tracking account" />
***
  </ToggleListItem>
<br />
  <ToggleListItem title="3. Enter tracking account details">
    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" src="https://files.readme.io/5b6205178ac4271906dd189c12eb20b185fd0546605101c222850d01caae5675-image.png" width="500px" />

    <br />

    <AsteridkForMandatoryElements />

    |         Element        | Description                                                                                                      |
    | :--------------------: | :--------------------------------------------------------------------------------------------------------------- |
    |      **Carrier**\*     | From the dropdown menu, select **InPost** as your carrier option.                                                |
    | **Shipping Account**\* | From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking. |
***
  </ToggleListItem>
<br />
  <ToggleListItem title="4. Save and add the tracking account">
    After entering all the necessary information, select ![alt text](https://files.readme.io/41bf635f2c82bf95197e5a2f62939d396ead6033e48a985a30965d84a5be57b8-Add_tracking_account_button_2.png).
  </ToggleListItem>
</ToggleList>

Once done, the InPost tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.

<br />
