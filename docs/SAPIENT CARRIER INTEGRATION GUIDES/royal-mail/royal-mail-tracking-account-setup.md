---
title: Add Royal Mail tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: false
icon: fad fa-calendar-circle-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add tracking accounts for Royal Mail to enhance visibility, improving customer interactions, and streamlining logistics operations for Royal Mail.

> 🚧 _Important_
>
> _Prior to adding a Royal Mail tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with Royal Mail._
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with Royal Mail._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

## How to add Royal Mail tracking account

To add a tracking account for Royal Mail in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Navigate to Tracking Accounts" icon="fa-route">
    <br />

    On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/86ec4af66edcc1841f0e501f76224d944ebc62c345dae8b6c66944c9ff8585c3-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select Add Tracking Account" icon="fa-plus-circle">
    <br />

    In the **Tracking Accounts** page, select ![](https://files.readme.io/c9db68351fac05183f1fb5e96c283dba68f88004061886b8c16c6da1b45a38ee-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/fdfcd880b84fd960b85197f1403debf6b591d0531f2ca13638b5fad703b4e560-Add_tracking_accounts_button.png" alt="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Fill in the tracking account details" icon="fa-file-alt">
    <br />

    On the **Add Tracking account** page, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/f2159cfc5df8047ce939baae8432347a35e1010906cc7596b53f8eca75c6cf46-Add_tracking_account_screen.png" alt="Adding tracking account" />
<br />
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
            From the dropdown menu, select Royal Mail as your carrier option.
          </td>
        </tr>

        <tr>
          <td>
            **Receive tracking after Delivered event**
          </td>

          <td>
            Turn the toggle on/off to perform the following operations:

            • Toggle on: to continue receiving any tracking events that occur after the final delivery in exceptional circumstances.

            • Toggle off (a default state): to stop receiving the tracking events after the final delivery.
          </td>
        </tr>

        <tr>
          <td>
            **Shipping Account**\*
          </td>

          <td>
            From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking.
          </td>
        </tr>
      </tbody>
    </Table>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4.  Submit the tracking account" icon="fa-check">
    <br />

    After entering all the necessary information, select ![](https://files.readme.io/024655253fdc0d7d670eb52d43cf3c30776a32082c8c99fd2c0d3cf2a7486fd5-Add_tracking_account_button_2.png).

    Once done, the Royal Mail tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
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
