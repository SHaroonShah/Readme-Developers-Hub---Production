---
title: Internation arrival containers (ASCAN) flow
deprecated: false
hidden: false
metadata:
  robots: index
---
Unlike the common Containers API, the [International arrival Containers](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/) endpoint is used for Royal Mail shipments that are being imported into UK only. For shipments in these containers, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with the `containerId` of the container, for better tracking and visibility purposes.

The following flows explain the entire journey of the containers with the shipments being transported into the UK.

## Create shipment and allocating container when the ContainerId is known

<Image align="center" width="1000px" src="https://files.readme.io/52b50d0cc4bfa6df5f69b1f36acf1c7f04dcc2e8b77f3ab56bb05989d466dca8-Flow_1.png" />