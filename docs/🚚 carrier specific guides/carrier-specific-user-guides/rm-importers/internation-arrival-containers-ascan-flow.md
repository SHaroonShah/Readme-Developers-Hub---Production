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