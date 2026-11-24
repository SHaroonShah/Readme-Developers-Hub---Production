---
title: Sandbox API development requirements
excerpt: >-
  Before you start testing in Sandbox, you must develop the required API calls
  listed below.
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
The Intersoft API is a RESTful API that uses JSON messages. Your system must be able to send and receive JSON messages in the format described in this documentation.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you use SAPIENT, you must authenticate your API requests using a&#x20;_<Glossary>bearer token</Glossary>_. for more information, refer to the&#x20;_[_Authentication_](https://docs.intersoftsapient.net/docs/authentication)_&#x20;section._

  _Please bear in mind that SAPIENT applies rate limits to all API requests. Your integration must be able to handle HTTP 429 responses when a rate limit is exceeded. For more information, refer to the&#x20;_[_API Rate Limiting_](https://docs.intersoftsapient.net/docs/api-rate-limiting)_&#x20;section._
</Callout>

You must develop the following API calls:

<Cards>
  <Card title="Create Shipment" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-solid fa-box" target="_blank">
    Generate the delivery <Glossary>labels</Glossary> for your packages.
  </Card>

  <Card title="Update Status to Cancel" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-ban" target="_blank">
    Cancel a shipment before it has been manifested.
  </Card>

  <Card title="Manifest Shipments" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode" icon="fa-solid fa-file-circle-check" target="_blank">
    Manifest your shipments to create the Royal Mail Sales Order Summary. This also sends the electronic pre-advice and billing data to Royal Mail.
  </Card>
</Cards>

<Callout icon="🚧" theme="warn">
  ### _Important_

  _You must manifest your shipments before they enter the Royal Mail network. If you do not manifest your shipments, this may cause delivery delays, missing tracking information, missing customer notifications, surcharges, or other issues._
</Callout>

<Accordion title="International Arrivals Containers (A-Scan) — Freight 2 Post customers only">
  The following API calls are mandatory for Freight 2 Post customers. You must manifest your Freight 2 Post shipments by container.

  <Cards>
    <Card title="Add Container" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm" icon="fa-solid fa-plus" target="_blank">
      Create an International Arrivals Container and assign an ID or alias.
    </Card>

    <Card title="Get Containers" href="https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm" icon="fa-solid fa-list" target="_blank">
      Get a list of all International Arrivals Containers set up on the system.
    </Card>

    <Card title="Update Container" href="https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-update-containerid" icon="fa-solid fa-pen-to-square" target="_blank">
      Update details of an International Arrivals Container.
    </Card>

    <Card title="Add / Remove Shipments" href="https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-arrows-left-right" target="_blank">
      Allocate shipments to a container or remove them before manifesting.
    </Card>

    <Card title="Delete Container" href="https://docs.intersoftsapient.net/reference/delete_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-trash" target="_blank">
      Delete a specific container.
    </Card>

    <Card title="Get Container" href="https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm-containerid" icon="fa-solid fa-magnifying-glass" target="_blank">
      Get details for a specific container.
    </Card>
  </Cards>
</Accordion>

<Callout icon="📘" theme="info">
  ### _Note_

  _If your servers are based in China, use the dedicated .cn API endpoints. Replace .net with .cn in the relevant endpoint URLs._

  _For example, when creating a new shipment replace the&#x20;_[https://api.intersoftsapient.net/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm)_&#x20;URL with&#x20;_[https://api.intersoftsapient.cn/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm)_._

  _Your integration should also support the .net endpoints as a backup._
</Callout>

***

### See also

<Cards columns="2">
  <Card title="Authentication" href="https://docs.intersoftsapient.net/docs/authentication" icon="fa-solid fa-lock" target="_blank">
    Set up your bearer token and authenticate API requests.
  </Card>
</Cards>