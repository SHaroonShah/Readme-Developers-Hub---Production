---
title: Add Spring GDS tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that enables the monitoring and
  logging of every possible real-time event related to a shipment throughout its
  lifecycle which is received via the SAPIENT tracking webhook.
deprecated: false
hidden: true
icon: fad fa-calendar-circle-plus
link:
  new_tab: false
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for Spring GDS to receive shipment tracking information.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Prior to adding a Spring GDS tracking account, make sure you have completed the following prerequisites:_

  1. _Enabled the&#x20;_[_label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with Spring GDS._
  2. _Enabled the&#x20;_[_tracking integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with Spring GDS._
  3. _Set up your&#x20;_<Glossary>tracking webhook</Glossary>_. For more information on how to set up a tracking webhook, refer to the&#x20;_[_Create tracking webhook_](https://docs.intersoftsapient.net/docs/create-tracking-webhook)_&#x20;section. This is a one-time activity, you do not have to do this every time you add a tracking account._

  _If you wish to receive tracking events via Intersoft using the tracking account you have created, make sure it is activated by the Spring GDS team._
</Callout>

## How to add a Spring GDS tracking account

To add a tracking account for Spring GDS in SAPIENT, follow these steps.

<ToggleList>
  <ToggleListItem title={<strong>1. Access tracking accounts page</strong>} icon="fa-rocket">
    <br />

    On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/f53608e208015447ef8f7fd5f987b3ecf8415f81e2736ec01c552a9c41436479-Tracking_accounts_tab.png" caption="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Select option to add new tracking account</strong>} icon="fa-rocket">
    <br />

    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/139bbda69af885f0824e5d5070ea342a6fb0a8d348c754389edb7a4dcfff7da2-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/78c8641717e62040ab3526e6706d6a1f3259fe7c85b2d92281d861538afc0ab8-Add_tracking_account_option.png" caption="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
    <br />

    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image src="https://files.readme.io/5a05049219932ce2eca5d134641828d27a97f321e20c6b9678f7f3714c8852b5-image.png" align="center" caption="Entering tracking account details" border={true} />

    <br />

    <AsteridkForMandatoryElements />

    |         Element        | Description                                                                                                      |
    | :--------------------: | :--------------------------------------------------------------------------------------------------------------- |
    |      **Carrier**\*     | From the dropdown menu, select **Spring GDS** as your carrier option.                     |
    | **Shipping Account**\* | From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking. |

    <br />

    > 📘 *Note*
    >
    > *If you wish to track every Spring GDS account created in SAPIENT, then you must add a tracking account for each one of them.*

    <br />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Complete setup </strong>} icon="fa-rocket">
    <br />

    After entering all the necessary information, select ![alt text](https://files.readme.io/ed87f1de8d9350f6fed52ac5c3b52ce0e63e2e6358aebac01389e9081c7b12d9-Add_tracking_account_button_2.png).

    Once done, the Spring GDS tracking account appears in the **Tracking Accounts** list. You can now receive tracking information on your <Glossary>shipments</Glossary>.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.04/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request" target="_blank">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up" target="_blank">
    Understand tracking events and milestone data.
  </Card>
</Cards>



