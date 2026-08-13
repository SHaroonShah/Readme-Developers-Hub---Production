---
title: Recall shipment
excerpt: >-
  Recalling a shipment refers to the process of reinstating or resuming the
  shipment that was previously cancelled.
deprecated: false
hidden: false
icon: fad fa-circle-arrow-left
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
After you have [cancelled](https://docs.intersoftsapient.net/docs/view-cancelled-shipments) the <Glossary>shipment</Glossary> in SAPIENT, you can anytime recall it and proceed with its processing. This might involve taking necessary actions to fulfil the order again after addressing the reasons for its cancellation.

<Cards>
  <Card title="UI Method" icon="fa-solid fa-desktop">
    Recall shipments directly through the SAPIENT user interface using the step-by-step process below.
  </Card>

  <Card title="API Method" icon="fa-solid fa-code">
    Use the SAPIENT API to programmatically recall shipments. View the API reference for detailed implementation.
  </Card>
</Cards>

## How to recall shipment

<Tabs>
  <Tab title="Recall via SAPIENT UI">
    To recall a shipment via the SAPIENT UI, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access cancelled shipments</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select the **Shipment Processing** > **Cancelled** option.

        <Image align="center" border={true} src="https://files.readme.io/3c65a988ba9ce65069de9aaffb097b351b1fc930b55dcb341690a1f3e178322d-Accessing_cancelled_shipments.png" caption="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select shipments to recall</strong>} icon="fa-rocket">
        <br />

        In the **Cancelled Shipments** page that opens, select the checkboxes next to the shipments you want to recall, and then select ![alt text](https://files.readme.io/79126340250abbe6f8c76ada767569f8015d1010731e0f45f0c35b2ea8e59fbd-Recall_shipments_button.png).

        <Image align="center" border={true} src="https://files.readme.io/7dd1d2279a2b79ecebfd8ec87b54829eed58a38965b0bbc8c851a26d7b97f86e-Recall_shipments_option.png" caption="Recalling shipment" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Confirm the action </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, select **Yes**.

        <Image align="center" src="https://files.readme.io/19f0b9332e273ee9df9bf4c94083980f8361c7ec4df29feb79081577da31ed54-Confirming_shipment_recalling.png" width="350px" caption="Confirming shipment recalling" />

        <br />

        Once confirmed, the shipment(s) is removed from the **Cancelled Shipments** list and goes back to its previous status and is ready for manifesting.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Recall via API">
    To recall shipment via our API, refer to the following endpoint:

    <Cards columns="2">
      <Card title="Update Status" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-code" target="_blank">
        Complete API reference for shipment status updates including recalling
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

## Key considerations

<Accordion title="Special Cases and Notes">
  ### Handling previously held shipments

  If the shipment was canceled while it was held and was recalled, then the recalled shipment goes back to the held status. If you wish to manifest it, then you must release it first.

  ### Bulk operations

  You can recall multiple shipments at once by selecting multiple checkboxes before clicking the recall button.

  ### Status restoration

  Recalled shipments automatically return to their previous status in the processing workflow, allowing you to continue where you left off.
</Accordion>
