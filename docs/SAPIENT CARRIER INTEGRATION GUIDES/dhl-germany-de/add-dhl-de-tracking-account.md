---
title: Add DHL DE tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that enables the monitoring and
  logging of every possible real-time event related to a shipment throughout its
  lifecycle which is received via the SAPIENT tracking webhook.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for DHL Germany  to enhance visibility, improving customer interactions, and streamlining logistics operations for DHL Germany.

> 🚧 _Important_
>
> _Prior to adding an DHL Germany tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with DHL Germany._
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with DHL Germany._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._
>
> _If you wish to receive the tracking events via INTERSOFT using the tracking account you have created, make sure it is is activated by the DHL Germany team._

## How to add DHL Germany tracking account

To add a tracking account for DHL Germany in SAPIENT, follow the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Navigate to the Tracking Accounts tab">
    In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/0b0bf418cd10c99ea179b79f676a9185f00ad99670333f70f1848e77f0ee2fef-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add tracking account">
    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/1797ee1f92c9e2a16f6b55d7a84e3ef14111e4ef4a7b3e13ff1acb538c1447e8-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/faca47a22b3d4de7d74e54c6ea663a5156625b787a81a5c7568d2ef0688da840-Add_tracking_account_button_EVRi.png" alt="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Enter tracking account details">
    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" src="https://files.readme.io/6f8492c7d2ea214fc444045c2540bea06c5468826e50660447fa4678b141c5a6-image.png" width="500px" />

    <br />

    <AsteridkForMandatoryElements />

    |         Element        | Description                                                                                                      |
    | :--------------------: | :--------------------------------------------------------------------------------------------------------------- |
    |      **Carrier**\*     | From the dropdown menu, select DHLDE - DHL Germany as your carrier option.                                       |
    | **Shipping Account**\* | From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking. |

    <br />

    > 📘 *Note*
    >
    > *To track data for every shipping account, you must create a tracking account for each.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="Step 4: Save and add the tracking account">
    After entering all the necessary information, select ![alt text](https://files.readme.io/f713760b5bde9e21d187c9b978502b434343e34f9f3db55afa5b565d35d478cd-Add_tracking_account_button_2.png).

    Once done, the DHL Germany tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>
</Cards>
