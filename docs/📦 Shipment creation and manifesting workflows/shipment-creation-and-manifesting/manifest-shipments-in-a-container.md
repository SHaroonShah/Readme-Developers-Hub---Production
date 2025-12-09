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
  <Card title="Destination-Based Segregation" icon="globe-americas">
    Manifest shipments to specific countries or regions on particular days of the week for better logistics planning.
  </Card>

  <Card title="Priority Processing" icon="bolt">
    Pack and send express delivery orders first, then handle standard shipments for optimized operations.
  </Card>
</Cards>

## How container manifesting works

You can create as many <Glossary>container</Glossary>(s) as you need and add numerous shipments to each container. Shipments in the container are manifested only when you manifest the container.

> 🚧 _Important_
>
> _Before manifesting the container, make sure of the following:_
>
> * _The**containerId** must be unique for each customer and can be reused after the container has been manifested._
> * _The containers can be manifested only via the API._

Once the container has been manifested, you can create a new container with the same name and repeat the process as needed.

### Workflow process

<Image align="center" alt="Workflow of manifesting shipment by container" border={false} caption="Workflow of manifesting shipment by container" src="https://files.readme.io/c426294f14151bd90d0a8cacc617a9e25f427a0974f4a4e0841350d8da0a5d0d-Manifest_by_container_flow.png" />
