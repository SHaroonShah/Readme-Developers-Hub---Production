---
title: API development requirements for Sandbox
excerpt: >-
  The development of some basic API calls is a process of creating and testing
  essential API functions that are fundamental to the operation of a software
  application. These initial API calls are typically recommended to handle core
  functionalities that the software can rely on once it is fully operational.
deprecated: false
hidden: false
icon: fad fa-circle-exclamation-check
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Intersoft API is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this section.

> 🚧 _Important_
>
> _Prior to going live on SAPIENT, provide a <Glossary>bearer token</Glossary>. See [Authentication](https://docs.intersoftsapient.net/docs/authentication) for details._

As a minimum, have the following API calls developed:

<Cards columns={3}>
  <Card title="Create Shipment" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-solid fa-box">
    Generate the delivery <Glossary>labels</Glossary> for your packages.
  </Card>

  <Card title="Update Status to Cancel" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-ban">
    Cancel/void a current shipping label. Can only be used before a <Glossary>shipment</Glossary> has been confirmed by being manifested.
  </Card>

  <Card title="Manifest Shipments" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode" icon="fa-solid fa-file-circle-check">
    Closeout shipments to produce the collection <Glossary>manifest</Glossary> (Royal Mail Sales Order Summary) and trigger electronic <Glossary>pre-advice</Glossary> and billing data to be sent to the <Glossary>carrier</Glossary>.
  </Card>
</Cards>

> 🚧 _Important_
>
> _Manifest your shipments before they enter the Royal Mail network. Not doing so may result in delays, missing tracking, lack of notifications for your end consumers, surcharges, and other issues._

<Accordion title="International Arrivals Containers (A-Scan) — Freight 2 Post customers only" icon="">
  These API calls are **mandatory for Freight 2 Post customers**. Freight 2 Post customers must manifest their shipments by container.

  <Cards columns={3}>
    <Card title="Add Container" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm" icon="fa-solid fa-plus">
      Create and name (with an ID or alias) a new International Arrivals Container for manifesting a specific group of shipments.
    </Card>

    <Card title="Get Containers" href="https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm" icon="fa-solid fa-list">
      Get a list of all International Arrivals Containers set up on the system.
    </Card>

    <Card title="Update Container" href="https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-update-containerid" icon="fa-solid fa-pen-to-square">
      Update details of an International Arrivals Container.
    </Card>

    <Card title="Add / Remove Shipments" href="https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-arrows-left-right">
      Allocate shipments to a container or remove them before manifesting.
    </Card>

    <Card title="Delete Container" href="https://docs.intersoftsapient.net/reference/delete_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-trash">
      Delete a specific container.
    </Card>

    <Card title="Get Container" href="https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-magnifying-glass">
      Get details for a specific container.
    </Card>
  </Cards>
</Accordion>

> 📘 _Note_
>
> _At INTERSOFT, we have developed a dedicated API endpoint for servers based in China.  To access this, kindly change your domain from **.net** to **.cn** for all the relevant endpoints you will be using._
>
> _For example, when creating a new shipment replace the[https://api.intersoftsapient.net/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm) URL with [https://api.intersoftsapient.cn/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm)._
>
> _As a back-up, please develop **.net** as well._

***

### See also

<Cards>
  <Card title="Authentication" href="https://docs.intersoftsapient.net/docs/authentication" icon="fa-solid fa-lock">
    Set up your bearer token and authenticate API requests.
  </Card>
</Cards>
