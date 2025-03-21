---
title: Internation arrival containers (ASCAN) flow
deprecated: false
hidden: false
metadata:
  robots: index
---
Unlike the common Containers API, the [International arrival Containers](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/) endpoint is used for Royal Mail shipments that are being imported into UK only. For shipments in these containers, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with the `containerId` of the container, for better tracking and visibility purposes.

The following flows explain the entire journey of the containers with the shipments being transported into the UK.

## Create shipment and allocate container when the ContainerId is known

<Image align="center" className="border" border={true} width="1000px" src="https://files.readme.io/4d5dd45d9f305de0d40db469ecfc7c8c395ebba991bdeec36ac69a5ca2e25d8f-Flow_1.png" />

The flowchart outlines a process for creating a shipment and allocating a container when the `ContainerId` is known, starting with the creation of a container in advance. Then it follows with the creation of an order and a shipment request. It checks for the presence of the `ContainerId`; if known, it retrieves container details and proceeds to populate required fields. If the shipment is successfully created, tracking numbers and labels are generated, leading to the printing of labels and preparation of the shipment for despatch. If any errors occur during the process, appropriate error responses are returned to ensure all issues are addressed systematically.

## Create shipment when containerId is unknown and allocating them later

<Image align="center" className="border" border={true} src="https://files.readme.io/2f89d2a4753066b08fa33913ccb06da98269f5c36c69e33dfb91aa6fefef7d31-Flow_2.png" />

The flow outlines the process of creating shipments when the `ContainerId` is unknown, which involves several key steps. First, an order is created by sending the [Create Shipment request](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm#/). If all required fields are populated, the shipment is successfully created, prompting the system to generate tracking numbers and labels. Subsequently, a container for a UK arrival is created, and a request to add a new container is sent. Shipments are allocated to the newly created container using an [Add/Remove Shipments request](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid#/), allowing up to 10,000 shipments to be linked to a single container before packing the shipment and finalising the process.

## Manifest container

<Image align="center" className="border" border={true} src="https://files.readme.io/6b0fa31d35b9ef08d803ba6952d1892219cb3c61fce8de145897aad1eec74f38-Flow_3.png" />

The flowchart outlines the process for managing shipments with Royal Mail. Initially, it checks if all shipments have been allocated; if so, the shipments are manifested and its details are sent to Royal Mail for processing, along with the container details. Once the containers arrive in the UK, the shipments are converted from Freight 2 Post and injected to the Royal Mail network.

As the shipments are in transit, tracking is initiated with a first tracking event triggered by the system. Subsequently, additional tracking events are logged upon reaching specific statuses, culminating in the delivery of the shipment, which is confirmed through a successful delivery trigger. If shipments have not been allocated, the process reverts to continue allocating shipments until all are accounted for.