---
title: Manifest shipments in a container
excerpt: >-
  Learn how to manifest shipments in containers to segregate and organize your
  shipping operations. Create containers, add multiple shipments, and manifest
  them together for better logistics management.
deprecated: false
hidden: false
icon: fad fa-truck-container
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
If your business process requires you to segregate the way you <Glossary>manifest</Glossary> your <Glossary>shipments</Glossary>, the **manifest by container** functionality provides the perfect solution for organizing your shipping operations.

<Cards columns={2}>
  <Card title="Destination-Based Segregation" icon="globe-americas">
    Manifest shipments to specific countries or regions on particular days of the week for better logistics planning.
  </Card>
  <Card title="Priority Processing" icon="bolt">
    Pack and send express delivery orders first, then handle standard shipments for optimized operations.
  </Card>
</Cards>

## How Container Manifesting Works

You can create as many <Glossary>container</Glossary>(s) as you need and add numerous shipments to each container. Shipments in the container are manifested only when you manifest the entire container, giving you complete control over the timing and grouping of your shipments.

<Columns layout="auto">
  <Column>
    **Flexible Organization**
    - Create unlimited containers
    - Add multiple shipments per container
    - Group shipments by any criteria
  </Column>
  <Column>
    **Controlled Manifesting**
    - Manifest entire containers at once
    - Choose optimal timing
    - Reuse container names after manifesting
  </Column>
</Columns>

<Accordion title="Important Requirements" icon="exclamation-triangle">

Before manifesting the container, make sure of the following:

* The **containerId** must be unique for each customer and can be reused after the container has been manifested.
* The containers can be manifested only via the API.

</Accordion>

## Container Lifecycle

Once the container has been manifested, you can create a new container with the same name and repeat the process as needed. This allows for efficient reuse of your container naming conventions while maintaining clear operational boundaries.

<Image alt="Workflow of manifesting shipment by container" align="center" src="https://files.readme.io/c426294f14151bd90d0a8cacc617a9e25f427a0974f4a4e0841350d8da0a5d0d-Manifest_by_container_flow.png">
  Workflow of manifesting shipment by container
</Image>

## Next Steps

Ready to implement container manifesting? Check out the API documentation for detailed implementation instructions and code examples.