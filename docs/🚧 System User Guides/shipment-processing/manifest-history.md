---
title: Manifest history
excerpt: >-
  The manifest history feature provides a comprehensive record of all shipping
  manifests generated over time. It is primarily used to review , track, and
  manage past shipments, ensuring visibility into shipping activities and
  helping with audit or compliance checks.
deprecated: false
hidden: false
icon: fad fa-rectangle-vertical-history
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can search and view manifested <Glossary>shipments</Glossary> based on <Glossary>customer</Glossary>, <Glossary>shipping location</Glossary>, and date ranges.\
To search manifested shipments in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Manifest History** option.

<Image alt="Accessing shipments" align="center" border={true} src="https://files.readme.io/2dd0be5964170ba8e4d0b9956c1c4cd105810b50071de35c1494e585185b5aa9-Manifest_history_option.png">
  Accessing manifest history
</Image>

2. In the **Manifest History** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![alt text](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png). 

> 📘 *Note*
>
> *The maximum date range for manifest search is 30 days*.

<Image alt="Specifying filters" align="center" border={true} src="https://files.readme.io/deeb8cf7c4927c2b815c757d722955250f58d02c85345f159c594a7fb238c59b-Manifest_history_filter.png">
  Specifying filters
</Image>

3. Once filtered, the **Manifest History** table displays the manifested shipments matching your search criteria. The columns displayed in the table are explained in the following table.

<Image alt="Viewing shipments" align="center" border={true} src="https://files.readme.io/7b056fb156b7f9215b4ed0ded2bc9a47f55ba8a45e473c7a72f7609259e26e52-Manifest_history_table.png">
  Viewing filtered shipments
</Image>

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Date**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the specific date when the manifest was created, crucial for tracking and historical reference.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Customer**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the  name or identifier of the customer associated with the shipment, helping to manage relationships and service levels.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipping Location**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the <Glossary>shipping location</Glossary> or dispatch point of the shipment, important for logistics planning and route optimisation.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipping Account**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the <Glossary>shipping account</Glossary> number linked to the shipments for billing and record-keeping purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Manifest Number**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the unique identifier assigned to each manifest, used for tracking and organizational purposes.  

        Select the manifest number link to open and download the <Glossary>manifest</Glossary> file either in <Glossary>CSV</Glossary> or <Glossary>PDF</Glossary>.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Carrier**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the name and logo of the <Glossary>carrier</Glossary> responsible for delivering the shipment.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Service**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Weight**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the total weight of the shipment included in the manifest, essential for billing and compliance.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Packages**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the total number of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Created**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the date and time when the manifest was generated, providing a timeline for shipping actions and record tracking.
      </td>
    </tr>
  </tbody>
</Table>

After viewing the manifest history, you can now return to the Home page and continue working with your ongoing shipments as needed.