---
title: Cancel Shipments
excerpt: >-
  Learn how to cancel shipments in SAPIENT through the UI or API. Shipments can
  be cancelled when they've been officially stopped and won't be delivered due
  to customer requests or logistical issues.
deprecated: false
hidden: false
icon: fad fa-nfc-slash
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    A shipment can be set to *Cancelled* when it has been officially stopped and
    is not going to be delivered. Cancellations may occur for various reasons,
    including customer requests or logistical issues.
  robots: index
---
In SAPIENT, you can cancel <Glossary>shipments</Glossary> to ensure that resources can be reallocated and allow users to manage customer expectations. The shipment can be canceled if it has been confirmed by being manifested.

<Cards columns="2">
  <Card title="UI Cancellation" icon="mouse-pointer">
    Cancel shipments directly through the SAPIENT interface with step-by-step guidance
  </Card>
  <Card title="API Cancellation" icon="code">
    Programmatically cancel shipments using our REST API endpoints
  </Card>
</Cards>

## How to Cancel Shipments

<Tabs>
  <Tab title="Via User Interface">
    
Follow these steps to cancel shipments through the SAPIENT UI:

### Step 1: Access Manifesting
In the side navigation panel, select **Shipment Processing** > **Manifesting**.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifesting option" src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" />

### Step 2: Configure Filters and Sorting
In the **Manifesting** page, you can:
- Sort the list by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
- Change the <Glossary>shipping location</Glossary> by selecting **Change Location**

<Image align="center" alt="Specifying filters" border={true} caption="Sorting list and changing location" src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" />

### Step 3: Apply Additional Filters
Filter the table data using:
- **Narrow by Status**: Filter by shipment status
- **Narrow by Service**: Filter by carrier service codes

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png" />

### Step 4: Select and Cancel Shipments
1. Next to the shipment you want to cancel, select ![alt text](https://files.readme.io/ade8694f40f0b89e1cfab543051a5b77f7a307552c22b1c0105f7f2439dd065e-View_button.png)
2. On the page that opens, select the checkbox next to the shipment
3. Click ![alt text](https://files.readme.io/ce57b2272ffff135c3c09d4b532c2cbff21b8ffeaaacb4bb668edcbd00c2e67c-Cancel_shipments_button.png)

<Image align="center" alt="Accessing option to cancel shipments" border={true} caption="Accessing option to cancel shipments" src="https://files.readme.io/1b5ebf0996d78e8b255de85c8da7e377d6f19524f9899bc8155d4b48f34ea0d0-Canceling_shipments.png" />

### Step 5: Confirm Cancellation
In the confirmation dialog:
1. Enter the reason for canceling the shipment
2. Select **Yes** to confirm

<Image align="center" alt="Confirming shipment cancellation" border={true} caption="Confirming shipment cancellation" src="https://files.readme.io/add229243a38970d994d96735c0f6ad74a1ca4404fa57475b6c9fc2a85b038ad-Confirming_shipment_cancellation.png" width="350px" />

  </Tab>
  <Tab title="Via API">
    
For programmatic shipment cancellation, use our REST API endpoints.

<Cards>
  <Card title="API Documentation" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="book">
    Complete API reference for shipment status updates including cancellation
  </Card>
</Cards>

### API Recipe Tutorial
For a detailed step-by-step process on canceling shipments via API:

<TutorialTile emoji="🦉" slug="cancel-and-release-shipments" title="Cancel shipments" />

  </Tab>
</Tabs>

## Post-Cancellation Information

<Accordion title="What Happens After Cancellation" icon="info-circle">
Once confirmed, the shipment(s) will be:
- Removed from the current manifesting list
- Displayed in the list of cancelled shipments
- Available for recall if needed using the [recall shipment feature](https://docs.intersoftsapient.net/docs/recall-shipment)
</Accordion>

## Viewing Cancelled Shipments

<Cards columns="2">
  <Card title="Quick Access" icon="eye">
    Select **View Cancelled Shipments** directly from the manifesting page
  </Card>
  <Card title="Navigation Menu" icon="bars">
    Access via **Shipment Processing** > **Cancelled** in the side navigation panel
  </Card>
</Cards>

<Image align="center" alt="Accessing canceled shipments" border={true} caption="Accessing cancelled shipments" src="https://files.readme.io/98bb78638eb05e979777dfd34b1a13605cab5520fa6017f7a980a02fc38a0602-Canceled_shipments_option.png" />