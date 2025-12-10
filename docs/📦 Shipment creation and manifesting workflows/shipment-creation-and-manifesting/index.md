---
title: Shipment creation and manifesting
excerpt: >-
  Shipment creation and manifesting are key processes in logistics, particularly
  in the context of transporting goods. _Shipment creation_ refers to the
  process of preparing and documenting the details of a shipment before it is
  despatched to its destination, whereas _manifesting_ is the process of
  creating a detailed list (manifest) of all shipments being handed over to the
  carrier.
deprecated: false
hidden: false
icon: fad fa-cart-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The SAPIENT API has been designed to accommodate different methods of processing <Glossary>shipments</Glossary> , to fit in with the varied ways many businesses operate their despatching function. This section provides a high-level overview on the different methods available to manage when to print labels and how to manifest accurately at the end of each working day.

> 📘 _Note_
>
> _For more detailed information, please contact the Intersoft Customer Operations team to arrange a consultation._

<Tabs>
  <Tab title="Shipment actions">
    ## Use shipment actions in Create Shipment API

    Shipment actions are specific operations that can be performed on a shipment during its lifecycle. These actions allow businesses to manage and control various aspects of the shipment process.

    <Cards columns="3">
      <Card title="Process" href="https://docs.intersoftsapient.net/docs/create-shipment-with-action-process" icon="cog">
        Finalises the shipment creation and prepares the shipment for transportation. A label is returned in the Create Shipment response and the shipment is ready for manifesting immediately.
      </Card>

      <Card title="Create" href="https://docs.intersoftsapient.net/docs/create-shipments-with-action-create" icon="plus-circle">
        Initiates a new shipment entry in the system. Captures all necessary details to generate shipping documents. Does not return labels immediately - requires Print Shipment API call.
      </Card>

      <Card title="Allocate" href="https://docs.intersoftsapient.net/docs/create-shipments-with-action-allocate" icon="boxes">
        Assigns resources (like inventory items) to the shipment for fulfilment. Returns carrier tracking number in Create Shipment response but requires Print Shipment API for labels.
      </Card>
    </Cards>

    ### Key differences

    * **Process**: Label generated immediately, ready for manifesting
    * **Create**: No immediate label or tracking number - generated when the Print Shipment API is called
    * **Allocate**: Tracking number provided immediately, label generated when Print Shipment API is called
  </Tab>

  <Tab title="Shipment status">
    ## Use shipment status in Update Shipment API

    The *shipment status* indicates the current state or condition of a shipment within the shipment process. Each status reflects a specific phase in the shipment lifecycle, providing visibility to both shippers and recipients.

    <Accordion title="Picked Status" icon="hand-paper">
      Indicates that the items for the shipment have been successfully collected from the inventory and are ready for the next steps in the shipment process.

      **Use case**: Print labels in advance by creating shipments using the **Process** action. When picked and ready to despatch, update the status to **Picked**. You can then manifest all picked shipments, ensuring unpicked shipments are not manifested.
    </Accordion>

    <br />

    <Accordion title="Release Status" icon="unlock">
      Indicates that the shipment has been authorised for despatch or has been cleared for shipment to the next destination.

      **Use case**: Manage approval workflows where shipments need authorisation before despatch.
    </Accordion>

    <br />

    <Accordion title="Cancel Status" icon="times-circle">
      Indicates that the shipment has been canceled and will not be processed any further.

      **Use case**: Prevents cancelled shipments from being included in manifests and carrier handovers.
    </Accordion>

    <br />

    <Accordion title="Hold Status" icon="pause-circle">
      Indicates that the shipment is temporarily paused and is not progressing to the next phases of fulfillment or transport until the necessary requirements are fulfilled.

      **Use case**: Temporarily delay shipments that are awaiting stock, payment, or other requirements. Only included in manifest production once released.
    </Accordion>

    <br />

    > 📘 *Note*
    >
    > *The "**Hold**" and "**Release**" statuses are available if a shipment needs to be delayed and only included in manifest production once it has been released.*
  </Tab>

  <Tab title="Containers">
    ## Using Containers

    Using the shipment status can be adopted for an operation to manage a fluid picking and packing set up. <Glossary>Containerisation</Glossary> allows users to manage shipments based on any number of variables.

    <Cards columns="2">
      <Card title="Carrier Sortation" icon="sort">
        For high volume users, your carrier may ask you to provide shipments pre-sorted based on service, destination or other factors. With containerisation, you can allocate shipments to a specific <Glossary>container</Glossary> and then manifest by container ID.

        **Examples**: Postcode sector, country code, or specific <Glossary>carrier</Glossary> service.
      </Card>

      <Card title="Managing Despatch Dates" icon="calendar">
        If you process pre-orders that need to be despatched on a specific date, a container ID could be set up for each date and shipments allocated based on requirements with the manifesting done by date, at container level.

        **Examples**: Date-based containers for scheduled releases or seasonal promotions.
      </Card>
    </Cards>

    <br />

    > 📘 *Note*
    >
    > *A container can be created with any Container ID that suits the needs of the organisation.*
  </Tab>

  <Tab title="Pre-allocate tracking">
    ## Pre-allocate tracking number API

    The <Glossary>pre-allocated tracking number</Glossary> API offers you the opportunity to request a pre-allocated Royal Mail tracking number for a destination and service.

    <Accordion title="When to Use Pre-allocation" icon="barcode">
      If your warehouse or eCommerce site operates in a way that you require a tracking number to be linked with your order, but you do not have the final details of your order yet, then consider using the [Pre Allocate Tracking Number](https://docs.intersoftsapient.net/reference/post_v4-shipments-preallocatetrackingnumber-rm) service.

      **Benefits**:

      * Link tracking numbers to orders early in the process
      * Minimal validation required for quick number allocation
      * Seamless integration with Create Shipment API
    </Accordion><br />

    <Accordion title="How It Works" icon="workflow">
      1. **Request pre-allocated tracking number** - Only minimal information required
      2. **Receive tracking number** - Issued without creating shipments or labels
      3. **Create shipment when ready** - Use the pre-allocated tracking number in the **PreAllocatedBarcode** object of the **Create Shipment** request
      4. **Platform creates shipment and label** - With your provided tracking number

      When requesting pre-allocated tracking number, only a small amount of information is passed in the request body and minimal validation is done to return a Royal Mail <Glossary>tracking number</Glossary>.
    </Accordion>

    <br />

    > 🚧 *Important*
    >
    > *Currently, this service is only available for Royal Mail services that have a 1D Tracking Number generated—this includes shipments using untracked services with the Royal Mail Recorded Signed for enhancement.*
  </Tab>
</Tabs>
