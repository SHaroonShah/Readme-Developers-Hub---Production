---
title: Add Amazon tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: true
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for Amazon to enhance visibility, improving customer interactions, and streamlining logistics operations for Amazon.

> 🚧 _Important_
>
> _Prior to adding an Amazon tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with Amazon._
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with Amazon._
> 3. _Set up your <Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._
>
> _If you wish to receive the tracking events via Intersoft using the tracking account you have created, make sure it is is activated by the Amazon team._

## How to add Amazon tracking account

To add a tracking account for Amazon in SAPIENT, follow the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access tracking accounts page</strong>} icon="fa-rocket">
    <br />

    On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/f53608e208015447ef8f7fd5f987b3ecf8415f81e2736ec01c552a9c41436479-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Select option to add new tracking account</strong>} icon="fa-rocket">
    <br />

    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/139bbda69af885f0824e5d5070ea342a6fb0a8d348c754389edb7a4dcfff7da2-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/78c8641717e62040ab3526e6706d6a1f3259fe7c85b2d92281d861538afc0ab8-Add_tracking_account_option.png" alt="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
    <br />

    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/8129682a2f6d552a7048f6beaafc0d4758263e28c6d9f5f8531ebb552867a182-Adding_tracking_account_Amazon.png" width="500px" alt="Adding tracking account" />

    <br />

    <AsteridkForMandatoryElements />

    |         Element        | Description                                                                                                      |
    | :--------------------: | :--------------------------------------------------------------------------------------------------------------- |
    |      **Carrier**\*     | From the dropdown menu, select AMAZON - Amazon as your carrier option.                                           |
    | **Shipping Account**\* | From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking. |

    <br />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Complete setup </strong>} icon="fa-rocket">
    <br />

    After entering all the necessary information, select ![alt text](https://files.readme.io/ed87f1de8d9350f6fed52ac5c3b52ce0e63e2e6358aebac01389e9081c7b12d9-Add_tracking_account_button_2.png).

    Once done, the Amazon tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="3">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>
