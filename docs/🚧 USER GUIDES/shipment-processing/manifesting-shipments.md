---
title: Manifest shipment
excerpt: >-
  Learn how to manifest shipments in SAPIENT through the UI, including filtering
  options, step-by-step procedures, and best practices for efficient shipment
  processing.
deprecated: false
hidden: false
icon: fad fa-cart-flatbed-empty
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
In SAPIENT, you can <Glossary>manifest</Glossary> <Glossary>shipment</Glossary>s using several methods:

<Cards columns="2">
  <Card title="Container-based manifesting" href="https://docs.intersoftsapient.net/docs/manifest-shipments-in-a-container" icon="box">
    Manifest shipments grouped within a specific container
  </Card>
  <Card title="Status-based manifesting" href="https://docs.intersoftsapient.net/docs/manifest-shipments-by-picked-status" icon="check-circle">
    Manifest shipments filtered by their Picked status
  </Card>
</Cards>

You can also manifest shipments by:
- Shipping location
- Shipping account  
- Service code

<Callout icon="💡" theme="default">
### Tip

You can manifest shipments both via UI and API. For API manifesting, refer to the <Anchor label="API References" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode">API References</Anchor> section.
</Callout>

## How to manifest a shipment

<Tabs>
<Tab title="Step-by-step process">

### 1. Access the manifesting page

In the side navigation panel, select **Shipment Processing** > **Manifesting**.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifesting option" src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" />

### 2. Configure your view

On the **Manifesting** page, you can:
- Sort the list by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
- Change the <Glossary>shipping location</Glossary> using the **Change Location** button

<Image align="center" alt="Specifying filters" border={true} caption="Sorting list and changing location" src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" />

### 3. Apply filters

Filter your shipments using:
- **Narrow by Status**: Filter by shipment status
- **Narrow by Service**: Filter by carrier service codes

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png" />

### 4. Initiate manifesting

Next to your desired shipment, select the manifest button: ![Manifest button](https://files.readme.io/fcb77ce4360ada3f172a0dccfceec28b483d6f4aa3e2a6a467929cf803686efe-Manifest_button.png)

<Image align="center" alt="Manifesting shipment" border={true} caption="Manifesting shipment" src="https://files.readme.io/417b398230fd2d49d159b9cc0cffa33e38496a2e5649b8fe2ec36d0a3078ce4a-Manifest_option.png" />

### 5. Confirm the manifest

Review the confirmation dialog carefully and select **Yes** if everything is correct.

<Image align="center" border={true} width="350px" src="https://files.readme.io/2b517ebeb7b8975acf72b7691c2d98aa3fd26d639e5ae366fdb98d5c5ae9d80e-Confirming_manifest.png" className="border" />

### 6. Monitor progress

You'll be directed to the **Manifest Processing Page** to track your manifest progress.

<Image align="center" alt="Processing manifest" border={true} caption="Processing manifest" src="https://files.readme.io/94ad18f86e7c082888deddcd6fd000efdf60439d19d1779d552b579fe3f219d1-Manifest_processing_page.png" />

### 7. View manifest details

Once processing is complete, expand the **Manifest/s processed** section using the view button: ![View manifests button](https://files.readme.io/b912251130f1a55af9a87de2cd47d96fa27576b740d7f5e4c4100d08470606d9-View_manifests_button.png)

<Image align="center" alt="Viewing manifest details" border={true} caption="Viewing manifest details" src="https://files.readme.io/a160eccb1432a48bba9e1295800375eb7307516e9c2fbcbb7d5f386f98648443-Manifest_details.png" />

</Tab>
<Tab title="Export options">

### Download manifest as PDF

Export your manifest file by selecting the **Download as PDF** icon ![PDF icon](https://files.readme.io/e12fc39d80fd5eb7931db6e1db22df354422aa16bbc2c675f70c85c4a788431c-PDF_icon.png) in the **Manifest Number** column.

### API processing

For automated processing, use the API recipe below:

<Recipe slug="process-shipments-created-with-the-action-process" title="Process shipment created with the action Process" />

</Tab>
</Tabs>

## Related resources

<Accordion title="Additional manifest resources" icon="book">

- <Anchor label="Set up manifest webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook">Set up manifest webhook</Anchor>
- <Anchor label="View manifest history" href="https://docs.intersoftsapient.net/docs/manifest-history">View manifest history</Anchor>

</Accordion>