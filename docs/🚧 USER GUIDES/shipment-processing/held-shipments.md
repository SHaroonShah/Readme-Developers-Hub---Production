---
title: Hold shipment
excerpt: >-
  Learn how to temporarily hold shipments in SAPIENT for up to 28 days,
  including prerequisites, step-by-step instructions, and important
  considerations for managing held shipments.
deprecated: false
hidden: false
icon: fad fa-sensor-triangle-exclamation
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
In SAPIENT, you can hold <Glossary>shipments</Glossary> for **28 days**. Shipments that are kept on hold longer than 28 days are cancelled automatically.

<Tabs>
<Tab title="Hold via UI">

<Accordion title="Prerequisites & Important Information" icon="info-circle">

**Before holding a shipment, make sure of the following:**

- You can only put shipments on hold that are in the **Label Printed** status, as only shipments with this status are included in manifests.
- If the shipments are released or taken off hold, they go back to the status from which they were kept on hold. For example, if the shipment was in the **Label Printed** status, after taking it off hold, it goes back to the **Label Printed** status.
- If the shipment was created 23 days ago and was taken off hold in the current date, it will be picked by manifesting with the current date and set this date as the actual shipment date—not the one created 23 days ago.

</Accordion>

## Step-by-Step Process

**1. Access Manifesting**

In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifesting option" src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" />

**2. Configure Filters and Sorting**

In the **Manifesting** page that opens, you can:
- Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
- Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

<Image align="center" alt="Specifying filters" border={true} caption="Sorting list and changing location" src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" />

**3. Apply Advanced Filters**

Filter the table data with the shipment status or carrier service by selecting the needed statuses and carrier service codes provided in the **Narrow by Status** and **Narrow by Service** blocks, respectively.

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png" />

**4. Select Shipments to Hold**

<Columns layout="auto">
<Column>

**For Bulk Operations:**
Next to the shipments that you want to hold, select ![alt text](https://files.readme.io/9a2d6ed673346e9c4c73e5a15a5dd8078483d6a780cf49d3f274cbf22c4df997-Hold_button.png).

</Column>
<Column>

**For Individual Shipments:**
Next to the shipment, select ![alt text](https://files.readme.io/b9b3f904604324043bea000c1255950ee01f735b7e665909e3bbd409faeb2956-View_button.png).

</Column>
</Columns>

**5. Confirm Hold Action**

On the page that opens, next to the shipment, select the checkbox and then click ![alt text](https://files.readme.io/1d487b18ddbdc249cef48fe35d465d2c89f5c7feb501f8cc797061ee607320cb-Hold_Shipments_button.png).

<Image align="center" alt="Accessing option to cancel shipments" border={true} caption="Accessing option to hold shipments" src="https://files.readme.io/3320e4d15decec9a248bb0a89c20e394b259c8c1368bd741773cd7814ed774c4-Hold_shipments_option.png" />

**6. Provide Hold Reason**

In the confirmation dialog that appears, from the dropdown menu, select the reason for holding the shipment, and then click **Yes**.

<Image align="center" alt="Confirming shipment cancellation" border={true} caption="Confirming shipment cancellation" src="https://files.readme.io/2ab6f56822de74b6346b1480d45c322673c372603a21ae06bb225425ba332f70-Conforming_shipment_hold.png" width="350px" />

Once confirmed, the shipment(s) is removed from the current list and is displayed in the list of held shipments.

</Tab>
<Tab title="Hold via API">

You can also hold shipments programmatically using the SAPIENT API.

<Cards columns={1}>
<Card title="API Reference" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="code">
For detailed information on how to hold shipments via API, refer to the API References section.
</Card>
</Cards>

</Tab>
</Tabs>

## Next Steps

<Cards columns={2}>
<Card title="Release Held Shipments" href="https://docs.intersoftsapient.net/docs/release-shipment" icon="unlock">
If needed, you can release the held shipments within the 28 days time frame and work with them accordingly.
</Card>
<Card title="View Held Shipments" icon="eye">
Access held shipments directly by selecting the **View Held Shipments** option or by accessing **Shipment Processing** > **Held** from the side navigation panel.
</Card>
</Cards>

<Image align="center" alt="Accessing canceled shipments" border={true} caption="Accessing held shipments" src="https://files.readme.io/bc5120461fe99089d00c1c83f39a4e5e0706b8a62d25f2c39b697cb4377bf6b4-Accessing_held_shipmehts.png" />