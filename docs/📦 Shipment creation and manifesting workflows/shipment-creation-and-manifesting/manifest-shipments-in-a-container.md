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
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If your business process requires you to segregate the way you <<glossary:manifest>> your <<glossary:shipments>> , for example, you might want to manifest the shipments to the USA or any other country on a particular day of the week, or you need to pack and send express delivery orders first, then you can achieve this by using the **manifest by container** functionality.

You can create as many <<glossary:container>>(s) as you need and add numerous shipments to each container. Shipments in the container are manifested only when you manifest the container.

> 🚧 _Important_
> 
> _Before manifesting the container, make sure of the following:_
> 
> - _The **containerId ** must be unique for each customer and can be reused after the container has been manifested._
> - _The containers can be manifested only via the API._

Once the container has been manifested, you can create a new container with the same name and repeat the process as needed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c426294f14151bd90d0a8cacc617a9e25f427a0974f4a4e0841350d8da0a5d0d-Manifest_by_container_flow.png",
        "",
        "Workflow of manifesting shipment by container"
      ],
      "align": "center",
      "caption": "Workflow of manifesting shipment by container"
    }
  ]
}
[/block]