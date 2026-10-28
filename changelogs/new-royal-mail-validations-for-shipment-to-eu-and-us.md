---
title: Royal Mail validation updates for shipments to EU and US
author: Syed Haroon Shah
hidden: false
metadata:
  robots: noindex
published_at: '2026-10-27T11:44:41.973Z'
type: added
---
Sapient has been updated to support additional shipment data required by Royal Mail for EU and US destinations:

<Table>
  <thead>
    <tr>
      <th>
        Destination
      </th>

      <th>
        Fields
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        B2C shipments to European Union (EU)
      </td>

      <td>
        - **SKUCode**
        - **ManufactureProductId**
        - **StandardisedProductId**
      </td>
    </tr>

    <tr>
      <td>
        Shipments to United States (US)
      </td>

      <td>
        - Shipper **ContactEmail** or **ContactPhone**
        - **PGAReferenceNumber**
      </td>
    </tr>
  </tbody>
</Table>

Where applicable, these fields will be subject to mandatory validation once the corresponding Royal Mail requirements are enforced.