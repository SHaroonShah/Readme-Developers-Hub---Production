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

In Option 1, create the International Arrival Container first and get the `ContainerId`. When you create a shipment, include the `ContainerId` to allocate the shipment to the container.<br />If the shipment is created successfully, the response returns the tracking number and Base64-encoded label. You can then decode and print the label and prepare the shipment for dispatch.<br />If required information is missing or incorrect, the shipment is not created and an error response is returned.

### Create shipment when containerId is unknown and allocating them later


<Image src="https://files.readme.io/97c8d939213ec0d082114c1b4fd8f46b2ddc42ddff3abd539626d0c21cc62f43-Flow_2.png" align="center" border={true} />


The flow outlines the process of creating shipments when the `ContainerId` is unknown, which involves several key steps. First, an order is created by sending the [Create Shipment request](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm#/). If all required fields are populated, the shipment is successfully created, prompting the system to generate tracking numbers and labels. Subsequently, a container for a UK arrival is created, and a request to add a new container is sent. Shipments are allocated to the newly created container using an [Add/Remove Shipments request](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid#/), allowing up to 10,000 shipments to be linked to a single container before packing the shipment and finalising the process.

### Manifest container


<Image src="https://files.readme.io/e29b772c2b3929f4f9950e2088f48fe8dc6bb679993a3029f3bd56747268b786-Flow_3.png" align="center" border={true} />


The flowchart outlines the process for managing shipments with Royal Mail. Initially, it checks if all shipments have been allocated; if so, the shipments are <Glossary>manifested</Glossary> and its details are sent to Royal Mail for processing, along with the container details. Once the containers arrive in the UK, the shipments are converted from Freight 2 Post and injected to the Royal Mail network.

As the shipments are in transit, tracking is initiated with a first tracking event triggered by the system. Subsequently, additional tracking events are logged upon reaching specific statuses, culminating in the delivery of the shipment, which is confirmed through a successful delivery trigger. If the expected number of shipments for that container have not been allocated, then you must revert back to continue allocating shipments until all are accounted for.


<Image src="https://files.readme.io/0fe72ecc237cd3cf26a2335f526ac2f68c9d2f65b921e5cea7554dd880ce1f72-ASCAN_label.jpg" align="center" width="400px" caption="Container barcode label example" border={true} />


***

### <br />See also

<Cards>
  <Card title="Set up Internatinal Arrival Containers barcode ranges" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers#/" icon="fa-solid fa-barcode-read" target="_blank">
    Configure a specific set of numbers designated for tracking containers arriving into the UK from overseas, facilitating efficient tracking and management.
  </Card>

  <Card title="Internation Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code" target="_blank">
    Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. Define which carrier and shipping location the container should be linked to.
  </Card>
</Cards>

<Cards columns="2">
  <Card title="A-Scan FAQs" href="https://docs.intersoftsapient.net/docs/a-scan-faqs#/" icon="fa-solid fa-messages-question">
    _Frequently asked questions regarding the International Arrivals Containers API/A-Scan._
  </Card>
</Cards>