---
title: Manifest shipments in a container
excerpt: >-
  Manifest shipments in a container is a process of creating a comprehensive
  document (manifest) that lists all the shipments packed within a specific
  container. This process serves as an essential record for logistics and
  shipping operations, detailing the contents of the container and providing
  critical information for transportation, customs clearance, and inventory
  management.
deprecated: false
hidden: false
icon: fad fa-truck-container
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If your business process requires you to segregate the way you <Glossary>manifest</Glossary> your <Glossary>shipments</Glossary> , for example, you might want to manifest the shipments to the USA or any other country on a particular day of the week, or you need to pack and send express delivery orders first, then you can achieve this by using the **manifest by container** functionality.

<Cards columns={2}>
  <Card title="Destination-based segregation" icon="fa-solid fa-globe">
    Manifest shipments to specific countries or regions on particular days of the week for better logistics planning.
  </Card>

  <Card title="Priority processing" icon="fa-solid fa-bolt">
    Pack and send express delivery orders first, then handle standard shipments for optimised operations.
  </Card>
</Cards>

<Callout icon="❗️" theme="error">
  ### _Caution_

  _If there are shipments in the container that cannot be manifested, the system will validate only the first 50 shipments and return any associated errors. However, the entire request will fail, and none of the shipments in the container will be manifested._
</Callout>

## How container manifesting works

You can create as many <Glossary>container</Glossary>(s) as you need and add numerous shipments to each container. Shipments in the container are manifested only when you manifest the container.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before manifesting the container, make sure of the following:_

  - _The&#x20;_**_containerId_**_&#x20;must be unique for each customer and can be reused after the container has been manifested._
  - _The containers can be manifested only via the API._
</Callout>

Once the container has been manifested, you can create a new container with the same name and repeat the process as needed.

### Workflow process


<Image src="https://files.readme.io/c426294f14151bd90d0a8cacc617a9e25f427a0974f4a4e0841350d8da0a5d0d-Manifest_by_container_flow.png" alt="Workflow of manifesting shipment by container" align="center" caption="Workflow of manifesting shipment by container" />


<br />