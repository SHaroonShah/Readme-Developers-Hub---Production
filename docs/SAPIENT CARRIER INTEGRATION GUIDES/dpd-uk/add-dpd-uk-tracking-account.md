---
title: Add DPD UK tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: false
icon: fad fa-calendar-clock
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for DPD UK to enhance visibility, improving customer interactions, and streamlining logistics operations for DPD UK.

> 🚧 _Important_
>
> _Prior to adding a DPD UK tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the <Anchor label="label integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> with DPD UK._
> 2. _Enabled the <Anchor label="tracking integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">tracking integration</Anchor> with DPD UK._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._
>
> _If you wish to receive the tracking events via Intersoft using the tracking account you have created, make sure it is is activated by the DPD UK team._

## How to add DPD UK tracking account

<ToggleList>
  <ToggleListItem title="Step 1. Navigate to the Tracking Accounts tab" icon="fa-arrow-right">
    On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/b8bf0b939dcc8227cc88b32d2ee0707e13bbfecbe7a5d116f0b6f6ac1de3303b-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />
***
  </ToggleListItem> <br />

  <ToggleListItem title="2. Select option to add a tracking account" icon="fa-arrow-right">
    In the **Tracking Accounts** page that opens, select ![](https://files.readme.io/f879cc7a233a578517b8e8034e326bc5c585f67b641db9adc93d3388d2a6fb78-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/522a3682f6e9a14eca2037dd25d5d2aa0972d04bd862883f5a35ac532f1ffce8-Add_tracking_account_button_DX.png" alt="Accessing option to add tracking account" />
***
  </ToggleListItem> <br />

  <ToggleListItem title="3. Enter tracking account details" icon="fa-arrow-right">
    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/0360cf8a986002fef3a87b152306907f660fb5c7f85e0f328e4f830b03b8a818-Adding_DPD_UK_tracking_account.png" width="500px" alt="Adding tracking account" />

    <AsteridkForMandatoryElements />

    <Table align={["center","left"]}>
      <thead>
        <tr>
          <th>
            Element
          </th>

          <th>
            Description
          </th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td>
            **Carrier**\*
          </td>

          <td>
            From the dropdown menu, select DPD UK as your carrier option.
          </td>
        </tr>

        <tr>
          <td>
            **Shipping Account**\*
          </td>

          <td>
            From the dropdown menu, select the shipping account for which you want to receive tracking.

            You can also select the **All Shipping Accounts** option to add this tracking account for all existing accounts.
          </td>
        </tr>
      </tbody>
    </Table>
***
  </ToggleListItem> <br />

  <ToggleListItem title="4. Save and add the tracking account" icon="fa-arrow-right">
    After entering all the necessary information, select ![](https://files.readme.io/2b94d65d1e560fcc17ab8e2c3e2af0c1e52b9dad2a1484f80ad7652b734ba1be-Add_tracking_account_button_2.png).

    Once done, the DPD UK tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
***
  </ToggleListItem> <br />
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
