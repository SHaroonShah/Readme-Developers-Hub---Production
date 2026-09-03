---
title: Swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2025-09-11T10:19:29.284Z'
type: improved
---
The following enhancements have been made to the swagger documentation:

* **Get PUDO Locations**. The following enhancements have been made to the **Get PUDO Locations** endpoint:
  * The **Get PUDO Locations** endpoint has been enhanced to integrate with the InPost **Locations Points** service, unlocking access to both Automated Parcel Machines (APMs or Lockers) and PUDO shop locations. This enhancement provides greater flexibility and convenience for customers choosing out-of-home delivery and return options.
  * The response example for the **Get PUDO Locations** endpoint in our Swagger documentation has been refined to reflect accurate, up-to-date data, ensuring greater clarity and reliability for customers integrating with our API.
  * The description of the **Labels** field in the Royal Mail Create Shipment response has been updated to reflect the generation of the ID8000 label—provided that the **PrintId8000Label** field in the request parameters is set to true.
  * The query and response field descriptions of all the DX API endpoints have been updated to improve clarity and support correct usage of the API.

<br />