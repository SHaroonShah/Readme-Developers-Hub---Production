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
    manifests generated over time. It is primarily used to review, track, and
    manage past shipments, ensuring visibility into shipping activities and
    helping with audit or compliance checks.
  robots: index
---
In SAPIENT, you can search and view manifested <Glossary>shipments</Glossary> based on <Glossary>customer</Glossary>, <Glossary>shipping location</Glossary>, and date ranges.  

## How to view manifest history

To search manifested shipments in SAPIENT, follow the steps as explained in the following procedure.

<br />

<ToggleList>
  <ToggleListItem title={<strong>1. Access the manifesting option</strong>} icon="fa-rocket">
    <br />

    In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

    <Image align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" alt="Accessing shipments" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Configure filters and sorting</strong>} icon="fa-rocket">
    <br />

    In the **Manifesting** page that opens, you can:

    * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
    * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

    <br />

    <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Apply additional filters </strong>} icon="fa-rocket">
    <br />

    In the **Manifesting** page that opens, you can:

    * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
    * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

    <br />

    <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Select shipments to hold </strong>} icon="fa-rocket">
    <br />

    Based on your requirements, select any of the following options:

    * **For bulk operations:**
      Next to the shipments that you want to hold, select ![alt text](https://files.readme.io/9a2d6ed673346e9c4c73e5a15a5dd8078483d6a780cf49d3f274cbf22c4df997-Hold_button.png).

    * **For individual shipments:**
      Next to the shipment, select ![alt text](https://files.readme.io/b9b3f904604324043bea000c1255950ee01f735b7e665909e3bbd409faeb2956-View_button.png).

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Confirm hold action</strong>} icon="fa-rocket">
    <br />

    On the page that opens, next to the shipment, select the checkbox and then click ![alt text](https://files.readme.io/1d487b18ddbdc249cef48fe35d465d2c89f5c7feb501f8cc797061ee607320cb-Hold_Shipments_button.png).

    <Image align="center" border={true} src="https://files.readme.io/3320e4d15decec9a248bb0a89c20e394b259c8c1368bd741773cd7814ed774c4-Hold_shipments_option.png" alt="Accessing option to cancel shipments" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>6. Provide reason for hold</strong>} icon="fa-rocket">
    <br />

    In the confirmation dialog that appears, from the dropdown menu, select the reason for holding the shipment, and then click **Yes**.

    <Image align="center" border={true} src="https://files.readme.io/2ab6f56822de74b6346b1480d45c322673c372603a21ae06bb225425ba332f70-Conforming_shipment_hold.png" width="350px" alt="Confirming shipment cancellation" />

    <br />

    Once confirmed, the shipments are removed from the current list and is displayed in the list of held shipments. If needed, you can [release the held shipments](https://docs.intersoftsapient.net/docs/release-shipment) within the 28 days time frame and work with them accordingly.
  </ToggleListItem>
</ToggleList>

1. In the side navigation panel, select the **Shipment Processing** > **Manifest History** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing manifest history" src="https://files.readme.io/2dd0be5964170ba8e4d0b9956c1c4cd105810b50071de35c1494e585185b5aa9-Manifest_history_option.png" />

2. In the **Manifest History** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png).

> 📘 _Note_
>
> _The maximum date range for manifest search is 30 days_.

<Image align="center" alt="Specifying filters" border={true} caption="Specifying filters" src="https://files.readme.io/deeb8cf7c4927c2b815c757d722955250f58d02c85345f159c594a7fb238c59b-Manifest_history_filter.png" />

3. Once filtered, the **Manifest History** table displays the manifested shipments matching your search criteria. The columns displayed in the table are explained in the following table.

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/7b056fb156b7f9215b4ed0ded2bc9a47f55ba8a45e473c7a72f7609259e26e52-Manifest_history_table.png" />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Column
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Date**
      </td>

      <td>
        Represents the specific date when the manifest was created, crucial for tracking and historical reference.
      </td>
    </tr>

    <tr>
      <td>
        **Customer**
      </td>

      <td>
        Represents the  name or identifier of the customer associated with the shipment, helping to manage relationships and service levels.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Location**
      </td>

      <td>
        Represents the <Glossary>shipping location</Glossary> or dispatch point of the shipment, important for logistics planning and route optimisation.
      </td>
    </tr>

    <tr>
      <td>
        **Shipping Account**
      </td>

      <td>
        Represents the <Glossary>shipping account</Glossary> number linked to the shipments for billing and record-keeping purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Manifest Number**
      </td>

      <td>
        Represents the unique identifier assigned to each manifest, used for tracking and organizational purposes.

        Select the manifest number link to open and download the <Glossary>manifest</Glossary> file either in <Glossary>CSV</Glossary> or <Glossary>PDF</Glossary>.
      </td>
    </tr>

    <tr>
      <td>
        **Carrier**
      </td>

      <td>
        Represents the name and logo of the <Glossary>carrier</Glossary> responsible for delivering the shipment.
      </td>
    </tr>

    <tr>
      <td>
        **Service**
      </td>

      <td>
        Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.
      </td>
    </tr>

    <tr>
      <td>
        **Weight**
      </td>

      <td>
        Represents the total weight of the shipment included in the manifest, essential for billing and compliance.
      </td>
    </tr>

    <tr>
      <td>
        **Packages**
      </td>

      <td>
        Represents the total number of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.
      </td>
    </tr>

    <tr>
      <td>
        **Created**
      </td>

      <td>
        Represents the date and time when the manifest was generated, providing a timeline for shipping actions and record tracking.
      </td>
    </tr>
  </tbody>
</Table>

After viewing the manifest history, you can now return to the Home page and continue working with your ongoing shipments as needed.