---
title: International Arrival Containers (A-Scan) flow
deprecated: false
hidden: false
icon: fad fa-container-storage
metadata:
  robots: index
---
The International [Arrival Containers (A-Scan)](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/) API is used for Royal Mail shipments being imported into the UK.

For shipments in an International Arrival Container, a<Glossary>Data Solution</Glossary> file is generated and sent to Royal Mail. This allows Royal Mail to link the shipments to the `ContainerId` for tracking and visibility.

Do not use the standard Containers API for Royal Mail Import shipments. Use the [International Arrival Containers (A-Scan) ](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/)API instead.<br /><br />You can create and allocate shipments to an International Arrival Container in two ways:

- **Option 1:** Create the container first. Then create the shipments and allocate them to the existing container using the `ContainerId`.
- **Option 2:** Create the shipments first. Then create the container and allocate the shipments to it.

Choose the option that best fits your integration. The diagrams below show the steps for each option.

### Option 1: Create the container before creating the shipment

The diagram below shows the Option 1 flow.

<Image src="https://files.readme.io/9bbca314d86f05e79fe4a8debb357a98b9c3176a7c47b4268a670f2b3c93fd90-ASCAN_flow_-_1.png" align="center" width="1000px" border={true} />

In Option 1, create the International Arrival Container first and get the `ContainerId`. When you create a shipment, include the `ContainerId` to allocate the shipment to the container.<br />If the shipment is created successfully, the response returns the tracking details and Base64-encoded label data. You can then decode and print the labels and prepare the shipment for dispatch.<br />If required information is missing or incorrect, the shipment is not created and an error response is returned.

### Option 2: Create the shipments before creating the container

The diagram below shows the Option 2 flow.

<Image src="https://files.readme.io/97c8d939213ec0d082114c1b4fd8f46b2ddc42ddff3abd539626d0c21cc62f43-Flow_2.png" align="center" border={true} />

In Option 2, create the shipments first without a `ContainerId`. If the shipments are created successfully, the response returns the tracking details and Base64-encoded label data. You can then decode and print the labels.<br />Next, create the International Arrival Container and get the `ContainerId`. Use the [Add/Remove Shipments ](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid#/)request to allocate the shipments to the container.<br />You can allocate up to 10,000 shipments to one container.<br />If required information is missing or incorrect, the shipment is not created and an error response is returned.

### Manifest container


<Image src="https://files.readme.io/e29b772c2b3929f4f9950e2088f48fe8dc6bb679993a3029f3bd56747268b786-Flow_3.png" align="center" border={true} />

Before manifesting the container, make sure all shipments have been allocated to it. If shipments are still missing, continue allocating them before you manifest the container.

When the container is ready, manifest it using the container details and `ContainerId`. The container and shipment details are then sent to Royal Mail, and the container label is returned.

The container can then be sent to the UK. When it arrives, the shipments enter the Royal Mail network for final delivery. Tracking events are generated as the shipments move through the Royal Mail network.

<Image src="https://files.readme.io/0fe72ecc237cd3cf26a2335f526ac2f68c9d2f65b921e5cea7554dd880ce1f72-ASCAN_label.jpg" align="center" width="400px" caption="Container barcode label example" border={true} />


***

### <br />Related guides

<Cards>
  <Card title="Set up Internatinal Arrival Containers barcode ranges" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers#/" icon="fa-solid fa-barcode-read" target="_blank">
    Set up the barcode range used to identify and track International Arrival Containers arriving in the UK.
  </Card>

  <Card title="Internation Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code" target="_blank">
    Create an International Arrival Container and assign an ID or alias. Select the carrier and Shipping Location linked to the container.
  </Card>
</Cards>

<Cards columns="2">
  <Card title="A-Scan FAQs" href="https://docs.intersoftsapient.net/docs/a-scan-faqs#/" icon="fa-solid fa-messages-question">
    Find answers to common questions about International Arrival Containers (A-Scan).
  </Card>
</Cards>
