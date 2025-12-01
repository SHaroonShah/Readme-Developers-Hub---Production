---
title: View manifest history
excerpt: >-
  The manifest history feature provides a comprehensive record of all shipping
  manifests generated over time. It is primarily used to review, track, and
  manage past shipments, ensuring visibility into shipping activities and
  helping with audit or compliance checks.
deprecated: false
hidden: false
icon: fad fa-rectangle-vertical-history
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    The manifest history feature provides a comprehensive record of all shipping
    manifests generated over time. It is primarily used to review , track, and
    manage past shipments, ensuring visibility into shipping activities and
    helping with audit or compliance checks.
  robots: index
---
In SAPIENT, you can search and view manifested <Glossary>shipments</Glossary> based on <Glossary>customer</Glossary>, <Glossary>shipping location</Glossary>, and date ranges.

<Cards columns={2}>
  <Card title="Quick Access" icon="shipping-fast">
    Navigate to **Shipment Processing** > **Manifest History** to get started with searching your manifested shipments.
  </Card>
  <Card title="Date Range Limit" icon="calendar-alt">
    **Important:** The maximum date range for manifest search is 30 days.
  </Card>
</Cards>

## How to Search Manifest History

<Accordion title="Step-by-Step Procedure" icon="list-ol">

### Step 1: Access Manifest History
In the side navigation panel, select the **Shipment Processing** > **Manifest History** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifest history" src="https://files.readme.io/2dd0be5964170ba8e4d0b9956c1c4cd105810b50071de35c1494e585185b5aa9-Manifest_history_option.png" />

### Step 2: Apply Filters
In the **Manifest History** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png).

<Image align="center" alt="Specifying filters" border={true} caption="Specifying filters" src="https://files.readme.io/deeb8cf7c4927c2b815c757d722955250f58d02c85345f159c594a7fb238c59b-Manifest_history_filter.png" />

### Step 3: View Results
Once filtered, the **Manifest History** table displays the manifested shipments matching your search criteria.

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/7b056fb156b7f9215b4ed0ded2bc9a47f55ba8a45e473c7a72f7609259e26e52-Manifest_history_table.png" />

</Accordion>

## Understanding the Manifest History Table

<Tabs>
  <Tab title="Basic Information">
    
**Date** - Represents the specific date when the manifest was created, crucial for tracking and historical reference.

**Customer** - Represents the name or identifier of the customer associated with the shipment, helping to manage relationships and service levels.

**Shipping Location** - Represents the <Glossary>shipping location</Glossary> or dispatch point of the shipment, important for logistics planning and route optimisation.

**Shipping Account** - Represents the <Glossary>shipping account</Glossary> number linked to the shipments for billing and record-keeping purposes.

  </Tab>
  
  <Tab title="Tracking & Logistics">
    
**Manifest Number** - Represents the unique identifier assigned to each manifest, used for tracking and organizational purposes. Select the manifest number link to open and download the <Glossary>manifest</Glossary> file either in <Glossary>CSV</Glossary> or <Glossary>PDF</Glossary>.

**Carrier** - Represents the name and logo of the <Glossary>carrier</Glossary> responsible for delivering the shipment.

**Service** - Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.

  </Tab>
  
  <Tab title="Package Details">
    
**Weight** - Represents the total weight of the shipment included in the manifest, essential for billing and compliance.

**Packages** - Represents the total number of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.

**Created** - Represents the date and time when the manifest was generated, providing a timeline for shipping actions and record tracking.

  </Tab>
</Tabs>

## Complete Column Reference

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>**Date**</td>
      <td>Represents the specific date when the manifest was created, crucial for tracking and historical reference.</td>
    </tr>
    <tr>
      <td>**Customer**</td>
      <td>Represents the name or identifier of the customer associated with the shipment, helping to manage relationships and service levels.</td>
    </tr>
    <tr>
      <td>**Shipping Location**</td>
      <td>Represents the <Glossary>shipping location</Glossary> or dispatch point of the shipment, important for logistics planning and route optimisation.</td>
    </tr>
    <tr>
      <td>**Shipping Account**</td>
      <td>Represents the <Glossary>shipping account</Glossary> number linked to the shipments for billing and record-keeping purposes.</td>
    </tr>
    <tr>
      <td>**Manifest Number**</td>
      <td>Represents the unique identifier assigned to each manifest, used for tracking and organizational purposes. Select the manifest number link to open and download the <Glossary>manifest</Glossary> file either in <Glossary>CSV</Glossary> or <Glossary>PDF</Glossary>.</td>
    </tr>
    <tr>
      <td>**Carrier**</td>
      <td>Represents the name and logo of the <Glossary>carrier</Glossary> responsible for delivering the shipment.</td>
    </tr>
    <tr>
      <td>**Service**</td>
      <td>Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.</td>
    </tr>
    <tr>
      <td>**Weight**</td>
      <td>Represents the total weight of the shipment included in the manifest, essential for billing and compliance.</td>
    </tr>
    <tr>
      <td>**Packages**</td>
      <td>Represents the total number of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.</td>
    </tr>
    <tr>
      <td>**Created**</td>
      <td>Represents the date and time when the manifest was generated, providing a timeline for shipping actions and record tracking.</td>
    </tr>
  </tbody>
</Table>

After viewing the manifest history, you can now return to the Home page and continue working with your ongoing shipments as needed.