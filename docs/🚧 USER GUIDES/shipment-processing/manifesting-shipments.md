---
title: Manifest shipment
excerpt: >-
  In this stage, shipments are being prepared for processing into a shipping
  manifest, which is a document listing all shipments to be sent together. This
  process involves gathering details about each shipment, allowing users to
  finalise the manifest and generate shipping labels for efficient despatch.
deprecated: false
hidden: false
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

> 💡 *Tip*
>
> *You can manifest the shipments both via UI and the API. For more information on how to manifest shipments via API, refer to the[API References](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) section.*

To manifest a shipment in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

<Image alt="Accessing shipments" align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png">
  Accessing manifesting option
</Image>

2. In the **Manifesting** page that opens, you can sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>. You can also change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button. 

<Image alt="Specifying filters" align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png">
  Sorting list and changing location
</Image>

3. Additionally, you can filter the table data with the shipment status or carrier service by selecting the needed statuses and carrier service codes provided in the **Narrow by Status** and **Narrow by Service** blocks, respectively. 

<Image alt="Viewing shipments" align="center" border={true} src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png">
  Viewing filtered shipments
</Image>

4. After you have filtered your desired shipments, next to the shipment that you want to manifest, select ![alt text](https://files.readme.io/fcb77ce4360ada3f172a0dccfceec28b483d6f4aa3e2a6a467929cf803686efe-Manifest_button.png). 

<Image alt="Manifesting shipment" align="center" border={true} src="https://files.readme.io/417b398230fd2d49d159b9cc0cffa33e38496a2e5649b8fe2ec36d0a3078ce4a-Manifest_option.png">
  Manifesting shipment
</Image>

5. In the confirmation dialog that appears, read the message carefully and if everything seems correct, then select **Yes**.

<Image align="center" className="border" width="350px" border={true} src="https://files.readme.io/2b517ebeb7b8975acf72b7691c2d98aa3fd26d639e5ae366fdb98d5c5ae9d80e-Confirming_manifest.png" />

6. After confirming the manifest request, you are directed to the **Manifest Processing Page**, where you can view the progress of your manifest. 

<Image alt="Processing manifest" align="center" border={true} src="https://files.readme.io/94ad18f86e7c082888deddcd6fd000efdf60439d19d1779d552b579fe3f219d1-Manifest_processing_page.png">
  Processing manifest
</Image>

7. After the manifest has been created successfully, in the **Manifest/s processed** block, select ![alt text](https://files.readme.io/b912251130f1a55af9a87de2cd47d96fa27576b740d7f5e4c4100d08470606d9-View_manifests_button.png) to expand the table with manifest details.

<Image alt="Viewing manifest details" align="center" border={true} src="https://files.readme.io/a160eccb1432a48bba9e1295800375eb7307516e9c2fbcbb7d5f386f98648443-Manifest_details.png">
  Viewing manifest details
</Image>

> 💡 *Tip*
>
> *You can export the manifest file by selecting the**Download as PDF** ![alt text](https://files.readme.io/e12fc39d80fd5eb7931db6e1db22df354422aa16bbc2c675f70c85c4a788431c-PDF_icon.png) icon in the **Manifest Number** column of the **Manifest/s processed** table.*

You have now successfully manifested your shipments.
