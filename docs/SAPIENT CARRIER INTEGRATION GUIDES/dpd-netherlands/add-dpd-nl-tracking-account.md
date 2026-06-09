---
title: Add DPD NL tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that enables the monitoring and
  logging of every possible real-time event related to a shipment throughout its
  lifecycle which is received via the SAPIENT tracking webhook.
deprecated: false
hidden: false
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for DPD Netherlands (NL)  to enhance visibility, improving customer interactions, and streamlining logistics operations for DPD NL.

> 🚧 _Important_
>
> _Prior to adding a DPD NL tracking account, make sure you have completed the following prerequisites:_
>
> 1. _Enabled the <Anchor label="label integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> with DPD NL._
> 2. _Enabled the <Anchor label="tracking integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">tracking integration</Anchor> with DPD NL._
> 3. _Set up your<Glossary>tracking webhook</Glossary>. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._
>
> _If you wish to receive the tracking events via Intersoft using the tracking account you have created, make sure it is is activated by the DPD NL team._

## How to add DPD NL tracking account

To add a tracking account for DPD NL in SAPIENT, follow the steps as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

<Image align="center" alt="Accessing tracking accounts" border={true} caption="Accessing tracking accounts" src="https://files.readme.io/b8bf0b939dcc8227cc88b32d2ee0707e13bbfecbe7a5d116f0b6f6ac1de3303b-Tracking_accounts_tab.png" />

2. In the **Tracking Accounts** page that opens, select ![](https://files.readme.io/f879cc7a233a578517b8e8034e326bc5c585f67b641db9adc93d3388d2a6fb78-Add_tracking_account_button.png).

<Image align="center" alt="Accessing option to add tracking account" border={true} caption="Accessing option to add tracking account" src="https://files.readme.io/522a3682f6e9a14eca2037dd25d5d2aa0972d04bd862883f5a35ac532f1ffce8-Add_tracking_account_button_DX.png" />

3. On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" caption="Adding tracking account" src="https://files.readme.io/a9185dc5d398a65874e330becae04968f4c6e26cdf54de202c35bae70ec1480f-image.png" width="500px" />

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
        **Carrier***
      </td>

      <td>
        From the dropdown menu, select DPD Netherlands as your carrier option.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Account***
      </td>

      <td>
        From the dropdown menu, select the shipping account for which you want to receive tracking.

        You can also select the **All Shipping Accounts** option to add this tracking account for all existing accounts.
      </td>
    </tr>
  </tbody>
</Table>

4. In the **SFTP DETAILS** form that opens, enter the necessary information as explained in the following table.

<Image align="center" caption="Entering SFTP details" src="https://files.readme.io/882dd7294f04765d960fd4f1e7863182d31c3a6d11c41e4504cd1dcd08fa0277-image.png" width="500px" />

<AsteridkForMandatoryElements />

|    Element    | Description                                                                                                               |
| :-----------: | :------------------------------------------------------------------------------------------------------------------------ |
| **Username*** | Enter the username that you have received from DPD NL in response to the tracking account setup request you sent earlier. |
| **Password*** | Enter the password that you have received from DPD NL in response to the tracking account setup request you sent earlier. |

5. After entering all the necessary information, select ![](https://files.readme.io/2b94d65d1e560fcc17ab8e2c3e2af0c1e52b9dad2a1484f80ad7652b734ba1be-Add_tracking_account_button_2.png).

Once done, the DPD NL tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.

<br />