---
title: Search shipments
excerpt: >-
  The *Shipment Search* feature is designed to serve as a tool for users to find
  and track shipments based on specific criteria.  The purpose is to provide
  visibility and updates on the status and details of shipments, helping users
  manage logistics more efficiently.
deprecated: false
hidden: false
icon: fad fa-print-magnifying-glass
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can search your <Glossary>shipments</Glossary> based on <Glossary>customer</Glossary>, <Glossary>shipping location</Glossary>, and date ranges.

<br />

<ToggleList>
  <ToggleListItem title={<strong>1. Access shipment search</strong>} icon="fa-rocket">
    <br />

      In the side navigation panel, select the **Shipment Search** option.

  <Image align="center" border={true} src="https://files.readme.io/61c56d1eac2f021d25812b6f6bda320ace57046cc188b77226161bca4a73963e-Shipment_search_option.png" alt="Accessing shipments" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Apply filters </strong>} icon="fa-rocket">
    <br />

     In the **Shipment Search** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![alt text](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png).

  > 📘 *Note*
  >
  > *The maximum date range for shipment search is 30 days*.

  <Image align="center" border={true} src="https://files.readme.io/f9ddcaf850dfd3eab60dd8b53e411e104e71000c4a4447df5a251a6368f39409-Shipment_search_filter.png" alt="Specifying filters" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. View search results </strong>} icon="fa-rocket">
    <br />

     Once filtered, the **Shipment Search** table displays the shipments matching your search criteria. The columns displayed in the table are explained in the following table.

  <Image align="center" border={true} src="https://files.readme.io/c285916b7f58433871d17666a0e9fc2aa38ea4b929a4cb089304fd5b608b87ba-Shipment_search_table.png" alt="Viewing shipments" />

  <Table align={["center","left"]}>
    <thead>
      <tr>
        <th>
          Element
        </th>

        <th>
          Description
        </th>
      </tr>
    </thead>

    <tbody>
      <tr>
        <td>
          **Tracking Number**
        </td>

        <td>
          Represents the unique identifier assigned to each shipment, allowing users to monitor its progress through the shipping system.

          Note: in this column, you can also download the shipment <Glossary>label</Glossary> or copy the <Glossary>tracking number</Glossary> by selecting the corresponding icons.
        </td>
      </tr>

      <tr>
        <td>
          **Shipment date**
        </td>

        <td>
          Represents  date on which the shipment was processed and dispatched, essential for tracking timelines and delivery expectations.
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
          **Account**
        </td>

        <td>
          Represents the account name associated with the shipment, used for billing and record-keeping purposes within the system.
        </td>
      </tr>

      <tr>
        <td>
          **Reference**
        </td>

        <td>
          Represents an additional identifier information, such as an order number or customer reference, providing context for the shipment.
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
          **Recipient**
        </td>

        <td>
          Represents the name of the individual or entity designated to receive the shipment, important for ensuring accurate delivery.
        </td>
      </tr>

      <tr>
        <td>
          **Destination**
        </td>

        <td>
          Represents  final location where the shipment is being sent, needed for route planning and logistical coordination.
        </td>
      </tr>

      <tr>
        <td>
          **Status**
        </td>

        <td>
          Represents  the current state of the shipment (for example, **Confirmed**, **Label Printed**, and so on), providing timely updates to users.
        </td>
      </tr>

      <tr>
        <td>
          **Packages**
        </td>

        <td>
          Represents quantity of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.
        </td>
      </tr>

      <tr>
        <td>
          **Last Modified**
        </td>

        <td>
          Represents the date and time of the most recent update to the shipment's information, helping users track changes and ensure accuracy.
        </td>
      </tr>
    </tbody>
  </Table>

    ***
  </ToggleListItem>
</ToggleList>

To search shipments in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Search** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing shipments" src="https://files.readme.io/61c56d1eac2f021d25812b6f6bda320ace57046cc188b77226161bca4a73963e-Shipment_search_option.png" />

2. In the **Shipment Search** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png).

> 📘 _Note_
>
> _The maximum date range for shipment search is 30 days_.

<Image align="center" alt="Specifying filters" border={true} caption="Specifying filters" src="https://files.readme.io/f9ddcaf850dfd3eab60dd8b53e411e104e71000c4a4447df5a251a6368f39409-Shipment_search_filter.png" />

3. Once filtered, the **Shipment Search** table displays the shipments matching your search criteria. The columns displayed in the table are explained in the following table.

<Image align="center" alt="Viewing shipments" border={true} caption="Viewing filtered shipments" src="https://files.readme.io/c285916b7f58433871d17666a0e9fc2aa38ea4b929a4cb089304fd5b608b87ba-Shipment_search_table.png" />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Element
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Tracking Number**
      </td>

      <td>
        Represents the unique identifier assigned to each shipment, allowing users to monitor its progress through the shipping system.

        Note: in this column, you can also download the shipment <Glossary>label</Glossary> or copy the <Glossary>tracking number</Glossary> by selecting the corresponding icons.
      </td>
    </tr>

    <tr>
      <td>
        **Shipment date**
      </td>

      <td>
        Represents  date on which the shipment was processed and dispatched, essential for tracking timelines and delivery expectations.
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
        **Account**
      </td>

      <td>
        Represents the account name associated with the shipment, used for billing and record-keeping purposes within the system.
      </td>
    </tr>

    <tr>
      <td>
        **Reference**
      </td>

      <td>
        Represents an additional identifier information, such as an order number or customer reference, providing context for the shipment.
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
        **Recipient**
      </td>

      <td>
        Represents the name of the individual or entity designated to receive the shipment, important for ensuring accurate delivery.
      </td>
    </tr>

    <tr>
      <td>
        **Destination**
      </td>

      <td>
        Represents  final location where the shipment is being sent, needed for route planning and logistical coordination.
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        Represents  the current state of the shipment (for example, **Confirmed**, **Label Printed**, and so on), providing timely updates to users.
      </td>
    </tr>

    <tr>
      <td>
        **Packages**
      </td>

      <td>
        Represents quantity of <Glossary>package</Glossary>s included in the shipment, vital for planning and inventory management.
      </td>
    </tr>

    <tr>
      <td>
        **Last Modified**
      </td>

      <td>
        Represents the date and time of the most recent update to the shipment's information, helping users track changes and ensure accuracy.
      </td>
    </tr>
  </tbody>
</Table>

After viewing your shipments, you can now take necessary actions on your shipments as needed.
