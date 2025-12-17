---
title: Add tracking account
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
To allow the system to automatically track <Glossary>shipments</Glossary> created on Intersoft SAPIENT and send tracking updates to the <Glossary>tracking webhook</Glossary> , the tracking accounts must be set up.

> 🚧 _Important_
>
> _Before setting up the tracking account, make sure that you have completed the following prerequisites:_
>
> 1. _Successfully [enabled the label and tracking integration](https://docs.intersoftsapient.net/docs/integration-activation) with your chosen <Glossary>carrier</Glossary> via the **Integration Activation** screen._
> 2. _Set up your tracking webhook. For more information on how to set up a tracking webhook, refer to the [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook) section. This is a one-time activity, you do not have to do this every time you add a tracking account._

## How to add tracking account

To add a tracking account in SAPIENT, follow the steps as explained in the following procedure.

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

    <Image align="center" border={true} src="https://files.readme.io/d5239464ffac95ad4b5081802a5b002a3e966e94ab27e760cf7ba3d2eeecaf56-Details_block_UPS.png" width="500px" alt="Adding tracking account" />
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
            From the dropdown menu, select the carrier for which you want to create a tracking account.
          </td>
        </tr>

        <tr>
          <td>
            **Shipping Account**\*
          </td>

          <td>
            From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking.

            For some carriers, you may also select the **All Shipping Accounts** option to add this tracking account for all existing and any new shipping accounts added to the customer account.
          </td>
        </tr>
      </tbody>
    </Table>
<br />
    Once entered, an additional **SFTP DETAILS** block may appear for specific carriers, for example YODEL and EVRi. This is only required if the carrier supports receiving the tracking details via SFTP (Secure File Transfer Protocol). For more information on how to fill this block, refer to the [Carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides) section.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Complete setup </strong>} icon="fa-rocket">
    <br />

    After entering all the necessary information, select ![alt text](https://files.readme.io/ed87f1de8d9350f6fed52ac5c3b52ce0e63e2e6358aebac01389e9081c7b12d9-Add_tracking_account_button_2.png).

    Once the tracking account is set up, any carrier tracking data for this account will be sent to your tracking webhook.
  </ToggleListItem>
</ToggleList>

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens, select the **Tracking Accounts** tab.

<Image align="center" alt="Accessing tracking accounts" border={true} caption="Accessing tracking accounts" src="https://files.readme.io/f53608e208015447ef8f7fd5f987b3ecf8415f81e2736ec01c552a9c41436479-Tracking_accounts_tab.png" />

2. In the **Tracking Accounts** page that opens, select ![](https://files.readme.io/139bbda69af885f0824e5d5070ea342a6fb0a8d348c754389edb7a4dcfff7da2-Add_tracking_account_button.png).

<Image align="center" alt="Accessing option to add tracking account" border={true} caption="Accessing option to add tracking account" src="https://files.readme.io/78c8641717e62040ab3526e6706d6a1f3259fe7c85b2d92281d861538afc0ab8-Add_tracking_account_option.png" />

3. On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Adding tracking account" border={true} caption="Adding tracking account" src="https://files.readme.io/d5239464ffac95ad4b5081802a5b002a3e966e94ab27e760cf7ba3d2eeecaf56-Details_block_UPS.png" width="500px" />

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
        From the dropdown menu, select the carrier for which you want to create a tracking account.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Account***
      </td>

      <td>
        From the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to receive tracking.

        For some carriers, you may also select the **All Shipping Accounts** option to add this tracking account for all existing and any new shipping accounts added to the customer account.
      </td>
    </tr>
  </tbody>
</Table>

4. Once entered, an additional **SFTP DETAILS** block may appear for specific carriers, for example YODEL and EVRi. This is only required if the carrier supports receiving the tracking details via SFTP (Secure File Transfer Protocol). For more information on how to fill this block, refer to the [Carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides) section.
5. After entering all the necessary information, select ![](https://files.readme.io/ed87f1de8d9350f6fed52ac5c3b52ce0e63e2e6358aebac01389e9081c7b12d9-Add_tracking_account_button_2.png).

Once the tracking account is set up, any carrier tracking data for this account will be sent to your tracking webhook.
