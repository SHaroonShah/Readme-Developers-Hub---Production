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

## How to search shipments in SAPIENT

To search shipments in SAPIENT, perform the steps as explained in the following procedure.

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

    <br />

    <Table align={["center", "left"]}>
      <thead>
        <tr>
          <th>Column</th>
          <th>Description</th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td><strong>Tracking Number</strong></td>
          <td>
            <p>Unique identifier assigned to each shipment, allowing you to monitor its progress through the shipping system.</p>
            <p>You can also download the shipment <Glossary>label</Glossary> or copy the <Glossary>tracking number</Glossary> by selecting the corresponding icons.</p>
          </td>
        </tr>

        <tr>
          <td><strong>Shipment date</strong></td>
          <td>Date on which the shipment was processed and dispatched.</td>
        </tr>

        <tr>
          <td><strong>Carrier</strong></td>
          <td>Name and logo of the <Glossary>carrier</Glossary> responsible for delivering the shipment.</td>
        </tr>

        <tr>
          <td><strong>Account</strong></td>
          <td>Account name associated with the shipment, used for billing and record-keeping purposes.</td>
        </tr>

        <tr>
          <td><strong>Reference</strong></td>
          <td>Additional identifier, such as an order number or customer reference, that provides context for the shipment.</td>
        </tr>

        <tr>
          <td><strong>Service</strong></td>
          <td>Shipping service used, such as standard or express.</td>
        </tr>

        <tr>
          <td><strong>Recipient</strong></td>
          <td>Name of the individual or entity designated to receive the shipment.</td>
        </tr>

        <tr>
          <td><strong>Destination</strong></td>
          <td>Final location where the shipment is being sent.</td>
        </tr>

        <tr>
          <td><strong>Status</strong></td>
          <td>Current state of the shipment, such as <strong>Confirmed</strong> or <strong>Label Printed</strong>.</td>
        </tr>

        <tr>
          <td><strong>Packages</strong></td>
          <td>Quantity of <Glossary>packages</Glossary> included in the shipment.</td>
        </tr>

        <tr>
          <td><strong>Last Modified</strong></td>
          <td>Date and time of the most recent update to the shipment's information.</td>
        </tr>
      </tbody>
    </Table>

    ***
  </ToggleListItem>
</ToggleList>