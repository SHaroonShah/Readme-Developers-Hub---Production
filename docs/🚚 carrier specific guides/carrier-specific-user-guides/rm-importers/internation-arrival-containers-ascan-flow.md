---
title: Internation arrival containers (ASCAN) flow
deprecated: false
hidden: false
metadata:
  robots: index
---
Unlike the common **Containers** API, the [International arrival Containers](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/) endpoint is used for Royal Mail <Glossary>shipments</Glossary> that are being imported into UK only. For shipments in these <Glossary>container</Glossary>s, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with the `containerId` of the container, for better tracking and visibility purposes.

Using this endpoint, you can either create the shipments and allocate the already created container (**Option 1**) or first create the shipments and then the container and later allocate your shipments to the container (**Option 2**).

Based on your business requirements, you may proceed with any of the preceding options and ship as needed. The following flows explain the entire journey of the UK arrival containers.

### Create shipment and allocate container when the ContainerId is known

<Image align="center" className="border" border={true} width="1000px" src="https://files.readme.io/5df9bc450c50a1edc88f858518058b4357749c69960cea101a8f706c9124b3c8-Flow_1.png" />

The flowchart outlines a process for creating a shipment and allocating a container when the `ContainerId` is known, starting with the creation of a container in advance. Then it follows with the creation of an order and a shipment request. It checks for the presence of the `ContainerId`; if known, it retrieves container details and proceeds to populate required fields. If the shipment is successfully created, <Glossary>tracking number</Glossary>s and <Glossary>labels</Glossary> are generated, leading to the printing of labels and preparation of the shipment for despatch. If any errors occur during the process, appropriate error responses are returned to ensure all issues are addressed systematically.

### Create shipment when containerId is unknown and allocating them later

<Image align="center" className="border" border={true} src="https://files.readme.io/97c8d939213ec0d082114c1b4fd8f46b2ddc42ddff3abd539626d0c21cc62f43-Flow_2.png" />

The flow outlines the process of creating shipments when the `ContainerId` is unknown, which involves several key steps. First, an order is created by sending the [Create Shipment request](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm#/). If all required fields are populated, the shipment is successfully created, prompting the system to generate tracking numbers and labels. Subsequently, a container for a UK arrival is created, and a request to add a new container is sent. Shipments are allocated to the newly created container using an [Add/Remove Shipments request](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid#/), allowing up to 10,000 shipments to be linked to a single container before packing the shipment and finalising the process.

### Manifest container

<Image align="center" className="border" border={true} src="https://files.readme.io/e29b772c2b3929f4f9950e2088f48fe8dc6bb679993a3029f3bd56747268b786-Flow_3.png" />

The flowchart outlines the process for managing shipments with Royal Mail. Initially, it checks if all shipments have been allocated; if so, the shipments are <Glossary>manifest</Glossary>ed and its details are sent to Royal Mail for processing, along with the container details. Once the containers arrive in the UK, the shipments are converted from Freight 2 Post and injected to the Royal Mail network.

As the shipments are in transit, tracking is initiated with a first tracking event triggered by the system. Subsequently, additional tracking events are logged upon reaching specific statuses, culminating in the delivery of the shipment, which is confirmed through a successful delivery trigger. If the expected number of shipments for that container have not been allocated, then you must revert back to continue allocating shipments until all are accounted for.

## See also

<Cards columns={4}>
  <Card title="Set up Internatinal Arrival Containers barcode ranges" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers#/" icon="fa-solid fa-barcode-read" target="_blank">
    Configure a specific set of numbers designated for tracking containers arriving into the UK from overseas, facilitating efficient tracking and management.
  </Card>

  <Card title="Internation Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code">
    *Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. Define which carrier and shipping location the container should be linked to.*
  </Card>

  <Card title="A-Scan FAQs" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code">
    *Frequently asked questions regarding the International Arrivals Containers API/A-Scan.*
  </Card>
</Cards>