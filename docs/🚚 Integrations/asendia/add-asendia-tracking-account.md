---
title: Add Asendia tracking account
excerpt: >-
  A _tracking account_ is a dedicated account that helps users, businesses, or
  customers to monitor and manage the status of shipments in real-time. This
  account provides access to tracking information for parcels and freight moving
  through logistics network or with specific carriers.
deprecated: false
hidden: true
icon: fad fa-calendar-circle-plus
metadata:
  robots: index
---
In SAPIENT, you can add tracking accounts for Asendia to enhance visibility, improving customer interactions, and streamlining logistics operations for Asendia.

Asendia’s tracking API uses separate credentials to the label API. Therefore, the Asendia tracking account screen will contain different customer’s credentials for the tracking API.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Prior to adding an Asendia tracking account, make sure you have completed the following prerequisites:_

  1. _Enabled the&#x20;_[_label integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with Asendia._
  2. _Enabled the&#x20;_[_tracking integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with Asendia._
  3. _Set up your&#x20;_<Glossary>tracking webhook</Glossary>_. For more information on how to set up a tracking webhook, refer to the&#x20;_[_Create tracking webhook_](https://docs.intersoftsapient.net/docs/create-tracking-webhook)_&#x20;section. This is a one-time activity, you do not have to do this every time you add a tracking account._
</Callout>

## How to add Asendia tracking account

To add a tracking account for Asendia in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Navigate to the Tracking Accounts tab">
    In the left navigation panel, select **API** > **Webhooks**. On the page that opens, select the **Tracking Accounts** tab.

    <Image align="center" border={true} src="https://files.readme.io/0b0bf418cd10c99ea179b79f676a9185f00ad99670333f70f1848e77f0ee2fef-Tracking_accounts_tab.png" caption="Accessing tracking accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add tracking account">
    In the **Tracking Accounts** page that opens, select ![alt text](https://files.readme.io/1797ee1f92c9e2a16f6b55d7a84e3ef14111e4ef4a7b3e13ff1acb538c1447e8-Add_tracking_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/faca47a22b3d4de7d74e54c6ea663a5156625b787a81a5c7568d2ef0688da840-Add_tracking_account_button_EVRi.png" caption="Accessing option to add tracking account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Enter tracking account details">
    On the **Add Tracking account** page that appears, in the **DETAILS** block, enter the necessary information as explained in the following table.

    
<Image src="https://files.readme.io/227b72cec9d3b71b42024fe9258fa26ba682b56704544ccbca466579071f8f1a-image.png" align="center" caption="Adding tracking account" border={true} />

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
            From the dropdown menu, select Asendia as your carrier option.
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
 <br />

    > 📘 *Note*
    >
    > *To track data for every shipping account, you must create a tracking account for each.*
    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Enter carrier tracking details">
    In the **SFTP DETAILS** block, enter the necessary information as explained in the following table:

    
<Image src="https://files.readme.io/9482eb1b0b8f53416db75c3a9ec827abf1bdf086b9700783842693380ff25ed3-image.png" align="center" caption="Entering carrier tracking details" border={true} />


    <br />

    <AsteridkForMandatoryElements />

    |     Element    | Description                                                                                                               |
    | :------------: | :------------------------------------------------------------------------------------------------------------------------ |
    | **ClientId**\* | Enter the Client ID provided by Asendia for authenticating the tracking account.   |
    | **ClientSecret**\* | Enter the Client Secret provided by Asendia for authenticating the tracking account.   |
 |  **AccessKey**\* | Enter the Access Key provided by Asendia for accessing the Tracking API. |
    |  **ApiKey**\* | Enter the API Key provided by Asendia for authorising Tracking API requests. |
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Save and add the tracking account">
    After entering all the necessary information, select ![alt text](https://files.readme.io/f713760b5bde9e21d187c9b978502b434343e34f9f3db55afa5b565d35d478cd-Add_tracking_account_button_2.png).<br />
    Once done, the Asendia tracking account is added successfully and appears in the **Tracking Accounts** list. You can now receive the tracking information on your <Glossary>shipments</Glossary>.
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


<Image src="https://files.readme.io/9482eb1b0b8f53416db75c3a9ec827abf1bdf086b9700783842693380ff25ed3-image.png" align="center" caption="Entering carrier tracking details" border={true} />