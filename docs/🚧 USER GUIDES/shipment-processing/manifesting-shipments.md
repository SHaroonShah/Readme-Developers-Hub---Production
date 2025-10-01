---
title: Manifest shipment
excerpt: >-
  In this stage, shipments are being prepared for processing into a shipping
  manifest, which is a document listing all shipments to be sent together. This
  process involves gathering details about each shipment, allowing users to
  finalise the manifest and generate shipping labels for efficient despatch.
deprecated: false
hidden: false
icon: fad fa-cart-flatbed-empty
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can <Glossary>manifest</Glossary> the <Glossary>shipment</Glossary>:

* [In a container](https://docs.intersoftsapient.net/docs/manifest-shipments-in-a-container)
* [By the Picked status](https://docs.intersoftsapient.net/docs/manifest-shipments-by-picked-status)

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can manifest the shipments both via UI and the API. For more information on how to manifest shipments via API, refer to the [API References](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) section._
</Callout>

To manifest a shipment in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifesting option" src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" />

2. In the **Manifesting** page that opens, you can sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>. You can also change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button.

<Image align="center" alt="Specifying filters" border={true} caption="Sorting list and changing location" src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" />

3. Additionally, you can filter the table data with the shipment status or carrier service by selecting the needed statuses and carrier service codes provided in the **Narrow by Status** and **Narrow by Service** blocks, respectively.

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png" />

4. After you have filtered your desired shipments, next to the shipment that you want to manifest, select ![](https://files.readme.io/fcb77ce4360ada3f172a0dccfceec28b483d6f4aa3e2a6a467929cf803686efe-Manifest_button.png).

<Image align="center" alt="Manifesting shipment" border={true} caption="Manifesting shipment" src="https://files.readme.io/417b398230fd2d49d159b9cc0cffa33e38496a2e5649b8fe2ec36d0a3078ce4a-Manifest_option.png" />

5. In the confirmation dialog that appears, read the message carefully and if everything seems correct, then select **Yes**.

<Image align="center" border={true} width="350px" src="https://files.readme.io/2b517ebeb7b8975acf72b7691c2d98aa3fd26d639e5ae366fdb98d5c5ae9d80e-Confirming_manifest.png" className="border" />

6. After confirming the manifest request, you are directed to the **Manifest Processing Page**, where you can view the progress of your manifest.

<Image align="center" alt="Processing manifest" border={true} caption="Processing manifest" src="https://files.readme.io/94ad18f86e7c082888deddcd6fd000efdf60439d19d1779d552b579fe3f219d1-Manifest_processing_page.png" />

7. After the manifest has been created successfully, in the **Manifest/s processed** block, select ![](https://files.readme.io/b912251130f1a55af9a87de2cd47d96fa27576b740d7f5e4c4100d08470606d9-View_manifests_button.png) to expand the table with manifest details.

<Image align="center" alt="Viewing manifest details" border={true} caption="Viewing manifest details" src="https://files.readme.io/a160eccb1432a48bba9e1295800375eb7307516e9c2fbcbb7d5f386f98648443-Manifest_details.png" />

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can export the manifest file by selecting the**Download as PDF** ![](https://files.readme.io/e12fc39d80fd5eb7931db6e1db22df354422aa16bbc2c675f70c85c4a788431c-PDF_icon.png) icon in the **Manifest Number** column of the **Manifest/s processed** table._
</Callout>

You have now successfully manifested your shipments.

To view a step-by-step process on how to create and manifest shipments via API, refer to the following API recipe:

<Recipe slug="process-shipments-created-with-the-action-process" title="Process shipment created with the action “Process”" />

**See also**

* [Set up manifest webhook](https://docs.intersoftsapient.net/docs/manifest-webhook#/)
* [Manifest shipments via UI](https://docs.intersoftsapient.net/docs/manifesting-shipments#/)
* [View manifest history](https://docs.intersoftsapient.net/docs/manifest-history#/)
