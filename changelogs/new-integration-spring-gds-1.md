---
title: New integration - Spring GDS
author: Syed Haroon Shah
hidden: true
published_at: '2026-10-05T16:01:42.091Z'
---
The Spring GDS integration has been added to the SAPIENT system. This integration supports shipping domestically within UK, to EU, and Rest of World (ROW) destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **Spring GDS&#x20;**&#x62;lock has been added to our carrier-specific APIs. This block includes the following API endpoints:

- **Shipping Account**
  - **Get Accounts**: Retrieve a list of the Spring GDS shipping accounts.
  - **Add Account**: Add a new Spring GDS shipping account.
  - **Get Account**: Retrieve details of a specific Spring GDS shipping account.
  - **Update Account**: Update details of an existing Spring GDS shipping account.
  - **Link Locations**: Link shipping locations to a Spring GDS shipping accounts.
  - **Get Associated Locations**: Retrieve locations linked to the Spring GDS shipping account.
  - **Get Associated Location**: Retrieve details for a specific Spring GDS associated location.
- **Shipments**
  - **Create Shipment**: Create a new Spring GDS shipment request.
  - **Print Label**: Generate a label for the Spring GDS shipment.
- **Spring GDS shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the Spring GDS shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes Spring GDS as a carrier for selection, with mandatory fields required for configuration.
- **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
- **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with Spring GDS.

<Callout icon="📘" theme="info">
  ### _Note_

  _For more information on this integration, refer to the&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/spring-gds">_Spring GDS_</Anchor>_&#x20;user guides._
</Callout>

<br />

<br />