---
title: Hold shipment
excerpt: >-
  This stage indicates that a shipment is temporarily paused, often due to
  specific issues such as missing information, payment verification, or
  compliance checks. Shipments in this stage require user intervention to
  resolve the problems and proceed with processing.
deprecated: false
hidden: false
icon: fad fa-sensor-triangle-exclamation
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can hold the <Glossary>shipments</Glossary> for 28 days. Shipments that are kept on hold longer than 28 days are cancelled automatically.

<Cards columns={2}>
  <Card title="UI Method" icon="fa-solid fa-desktop">
    Hold shipments directly through the SAPIENT user interface using the step-by-step process below.
  </Card>

  <Card title="API Method" icon="fa-solid fa-code">
    Use the SAPIENT API to programmatically hold shipments. View the API references for detailed implementation.
  </Card>
</Cards>

<Accordion title="Prerequisites and important information" icon="info-circle">
  Before holding a shipment, make sure of the following:

  * You can only put shipments on hold that are in the **Label Printed** status, as only shipments with this status are included in manifests.
  * If the shipments are released or taken off hold, they go back to the status from which they were kept on hold. For example, if the shipment was in the **Label Printed** status, after taking it off hold, it goes back to the **Label Printed** status.
  * If the shipment was created 23 days ago and was taken off hold in the current date, it will be picked by manifesting with the current date and set this date as the actual shipment date—not the one created 23 days ago.
</Accordion>

## How to hold shipment

<Tabs>
  <Tab title="Hold via SAPIENT UI">
    

    To hold a shipment in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the manifesting option</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

        <Image align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" caption="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Configure filters and sorting</strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can:

        * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" caption="Specifying filters" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Apply additional filters </strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can:

        * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" caption="Specifying filters" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Select shipments to hold </strong>} icon="fa-rocket">
        <br />

        Based on your requirements, select any of the following options:

        * **For bulk operations:**
          Next to the shipments that you want to hold, select ![alt text](https://files.readme.io/9a2d6ed673346e9c4c73e5a15a5dd8078483d6a780cf49d3f274cbf22c4df997-Hold_button.png).

        * **For individual shipments:**
          Next to the shipment, select ![alt text](https://files.readme.io/b9b3f904604324043bea000c1255950ee01f735b7e665909e3bbd409faeb2956-View_button.png).

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Confirm hold action</strong>} icon="fa-rocket">
        <br />

        On the page that opens, next to the shipment, select the checkbox and then click ![alt text](https://files.readme.io/1d487b18ddbdc249cef48fe35d465d2c89f5c7feb501f8cc797061ee607320cb-Hold_Shipments_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3320e4d15decec9a248bb0a89c20e394b259c8c1368bd741773cd7814ed774c4-Hold_shipments_option.png" caption="Accessing option to cancel shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Provide reason for hold</strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, from the dropdown menu, select the reason for holding the shipment, and then click **Yes**.

        <Image align="center" border={true} src="https://files.readme.io/2ab6f56822de74b6346b1480d45c322673c372603a21ae06bb225425ba332f70-Conforming_shipment_hold.png" width="350px" caption="Confirming shipment cancellation" />

        <br />

        Once confirmed, the shipments are removed from the current list and is displayed in the list of held shipments. If needed, you can [release the held shipments](https://docs.intersoftsapient.net/docs/release-shipment) within the 28 days time frame and work with them accordingly.
      </ToggleListItem>
    </ToggleList>

    <Callout icon="💡" theme="default">
      ### *Tip*

      *You can access the held shipments directly from this page by selecting the**View Held Shipments** option or by accessing the **Shipment Processing** > **Held** option from the side navigation panel.*

      <Image align="center" border={true} src="https://files.readme.io/bc5120461fe99089d00c1c83f39a4e5e0706b8a62d25f2c39b697cb4377bf6b4-Accessing_held_shipmehts.png" caption="Accessing canceled shipments" />
    </Callout>
  </Tab>

  <Tab title="Hold via API">
    To hold shipment via our API, refer to the following endpoint

    <Cards>
      <Card title="Update Status" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-code">
        Complete API reference for shipment status updates including holding
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />
