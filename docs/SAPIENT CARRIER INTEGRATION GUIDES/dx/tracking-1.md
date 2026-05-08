---
title: Add DX Express tracking account
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
In SAPIENT, you can add tracking accounts for DX Express to enhance visibility, improving customer interactions, and streamlining logistics operations for DX.

> 🚧 *Important*
>
> *Prior to adding a DX tracking account, make sure you have completed the following prerequisites:*
>
> 1. *Enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) with DX Express.*
> 2. *Enabled the [tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with DX Express.*
> 3. *Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account.*
>
> *Also, if you already have an account with DX Express that is actively being used, and if you wish to receive tracking via Intersoft, you need to request a new account number in order to integrate with Intersoft. This request can be made to your DX account manager. Make sure this is done before you can set up a tracking account.*

To add a tracking account for DX Express in SAPIENT, follow the steps as explained in the following procedure.

<ToggleList>

<ToggleListItem title="Step 1: Open Tracking Accounts">

On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

<Image align="center" alt="Accessing tracking accounts" border={true} caption="Accessing tracking accounts" src="https://files.readme.io/b8bf0b939dcc8227cc88b32d2ee0707e13bbfecbe7a5d116f0b6f6ac1de3303b-Tracking_accounts_tab.png" />

</ToggleListItem>

<ToggleListItem title="Step 2: Add a tracking account">

In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/f879cc7a233a578517b8e8034e326bc5c585f67b641db9adc93d3388d2a6fb78-Add_tracking_account_button.png).

<Image align="center" alt="Accessing option to add tracking account" border={true} caption="Accessing option to add tracking account" src="https://files.readme.io/522a3682f6e9a14eca2037dd25d5d2aa0972d04bd862883f5a35ac532f1ffce8-Add_tracking_account_button_DX.png" />

</ToggleListItem>

<ToggleListItem title="Step 3: Enter tracking account details">

On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Adding tracking account" border={true} caption="Adding tracking account" src="https://files.readme.io/1b4b82b250370e66282af5e304070a09a935b19cd81f819d09576ae90d560271-Details_block_DX.png" width="500px" />

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
        From the dropdown menu, select DX as your carrier option.
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

</ToggleListItem>

<ToggleListItem title="Step 4: Save the tracking account">

After entering all the necessary information, select ![alt text](https://files.readme.io/2b94d65d1e560fcc17ab8e2c3e2af0c1e52b9dad2a1484f80ad7652b734ba1be-Add_tracking_account_button_2.png).

</ToggleListItem>

</ToggleList>

Once done, the DX Express tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.