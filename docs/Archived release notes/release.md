---
title: Release
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<details>
  <summary>Release notes 2025</summary>

  <br />

  **Receive tracking events after the ‘Delivered’ event**\
  Each tracking account screen now can receive tracking events after the ‘Delivered’ event to enhance the customer’s visibility of their Royal Mail shipment tracking. With it, customers can easily manage their settings through the Add, Edit, and View tracking account screens for Royal Mail, ensuring they receive timely and accurate push notifications on their shipments—and can still choose to receive the events recorded after the delivered event. This enhancement features the logic update of the Sapient system to generate push payloads for Royal Mail tracking accounts based on the newly defined UI setting and the time elapsed since a ‘Delivered’ tracking event.

  ***

  **Swagger documentation updates**\
  The following updated have been made to the swagger documentation:

  * ID8000 Category fields description and available values are updated in Hazmat Information element in Royal Mail Create Shipment Request and APIs under Products section.
  * Error Responses for HTTP 400 error has been updated in the Get Time Zones API under Reference Data section.\
    Section Description has been updated in the Get Collections Timeslots, Book Collection and Cancel Collection APIs under Collections section in Royal Mail API.

  ***

  **Royal Mail Integration**\
  The Royal Mail Create Shipment API response now includes the ‘PartnerDetails’ field. This field is populated when a partnerLabel is used and left blank when a partnerLabel is not used for the shipment. For more information on creating a Royal Mail shipment, please refer to the API reference page and the Royal Mail API section.
</details>

***

<details>
  <summary><strong>Release notes 2025</strong></summary>

  <br />

  **Receive tracking events after the ‘Delivered’ event**\
  Each tracking account screen now can receive tracking events after the ‘Delivered’ event to enhance the customer’s visibility of their Royal Mail shipment tracking. With it, customers can easily manage their settings through the Add, Edit, and View tracking account screens for Royal Mail, ensuring they receive timely and accurate push notifications on their shipments—and can still choose to receive the events recorded after the delivered event. This enhancement features the logic update of the Sapient system to generate push payloads for Royal Mail tracking accounts based on the newly defined UI setting and the time elapsed since a ‘Delivered’ tracking event.

  ***

  **Swagger documentation updates**\
  The following updated have been made to the swagger documentation:

  * ID8000 Category fields description and available values are updated in Hazmat Information element in Royal Mail Create Shipment Request and APIs under Products section.
  * Error Responses for HTTP 400 error has been updated in the Get Time Zones API under Reference Data section.\
    Section Description has been updated in the Get Collections Timeslots, Book Collection and Cancel Collection APIs under Collections section in Royal Mail API.

  ***

  **Royal Mail Integration**\
  The Royal Mail Create Shipment API response now includes the ‘PartnerDetails’ field. This field is populated when a partnerLabel is used and left blank when a partnerLabel is not used for the shipment. For more information on creating a Royal Mail shipment, please refer to the API reference page and the Royal Mail API section.
</details>

<div className="rounded-md border border-gray-200 bg-white p-5 shadow-sm dark:border-white/10 dark:bg-inherit">
  <Cards columns={3}>
    <Card title="First Card" href="https://readme.com" icon="fa-home" iconColor="blue" tooltip="Go to ReadMe">
      *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
    </Card>

    <Card title="Third Card" icon="fa-star" iconColor="blue-500">
      `Ut enim ad minim veniam, quis nostrud ullamco`
    </Card>

    <Card title="Fourth Card" icon="fa-question" iconColor="blue-500" tooltip="Help & FAQs">
      **Excepteur sint occaecat cupidatat non proident**
    </Card>
  </Cards>
</div>
