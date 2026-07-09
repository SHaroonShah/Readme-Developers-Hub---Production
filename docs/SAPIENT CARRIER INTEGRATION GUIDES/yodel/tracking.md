---
title: Add YODEL tracking account
excerpt: >-
  A tracking account is a dedicated account that helps users, businesses, or
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
In SAPIENT, you can add tracking accounts for YODEL to enhance visibility, improving customer interactions, and streamlining logistics operations for YODEL.

Before adding a YODEL tracking account, you need to [send a corresponding request to YODEL](mailto:ISSOnbording@Yodel.co.uk) via email with the subject line “*Intersoft (your client name) STFP IOD tracking request*”. In the body of the email, make sure to add the following details:

***\[Your client name] would like IOD tracking enabled for the following Yodel contract number (7 digit number). Please respond to this email with the SFTP username and password and file naming convention for IOD tracking files.***

> 🚧 _Important_
>
> _Prior to adding a YODEL tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with YODEL._
> 2. _Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with YODEL._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

## How to add YODEL tracking account

To add a tracking account for YODEL in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Navigate to the Tracking Accounts tab">
    In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/3812e0d15bd2f19f64f9644a82d88a1ce95254d34f89ba7eb5de616c9fd0ff3c-Tracking_accounts_tab.png" alt="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add tracking account">
    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/647be94f894111181386f1ec3cdd959a85938dd4c0cd8d123d206b7db0487c8d-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/f95d0d1892b2dd558068c2cb28e4885997e9341c545c83c597ba1134c74e73ea-Add_tracking_accounts_button_YODEL.png" alt="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Enter tracking account details">
    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/e2b0cbf7a01deef853dcf1fddd0b7bbc151c981730d577b226c9e99c6166cb26-Details_block_YODEL.png" width="500px" alt="Adding tracking account" />

    <br />

    <AsteridkForMandatoryElements />

    <table>
      <thead>
        <tr>
          <th>Element</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Carrier</strong>&#42;</td>
          <td>From the dropdown menu, select YODEL as your carrier option.</td>
        </tr>
        <tr>
          <td><strong>Shipping Account</strong>&#42;</td>
          <td>
            From the dropdown menu, select the shipping account for which you want to receive tracking.
            <br />
            <br />
            You can also select the <strong>All Shipping Accounts</strong> option to add this tracking account for all existing accounts.
          </td>
        </tr>
      </tbody>
    </table>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Enter SFTP details">
    In the **SFTP DETAILS** block, enter the necessary information as explained in the following table:

    <Image align="center" src="https://files.readme.io/b2437869c8baecd092365fb5631a2dc0e31e07454c824245442ab67bc10ec14c-SFTP_details_block_EVRi.png" width="500px" />

    <br />

    <AsteridkForMandatoryElements />

    |     Element    | Description                                                                                                                |
    | :------------: | :------------------------------------------------------------------------------------------------------------------------- |
    | **Username**\* | Enter the username that you have received from YODEL in response to the tracking account setup request you sent earlier.   |
    | **Password**\* | Enter the password that you have received from YODEL in response to the tracking account setup request you sent earlier.   |
    |  **File Path** | Enter the file path that you have received from YODEL in response to your tracking account setup request you sent earlier. |
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Save and add the tracking account">
    After entering all the necessary information, select ![alt text](https://files.readme.io/d653c1f7e04a77a0bca6247e1bcbca03ccf933465c63ed23d2aa17b63243a632-Add_tracking_account_button_2.png).<br />
    Once done, the YODEL tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
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