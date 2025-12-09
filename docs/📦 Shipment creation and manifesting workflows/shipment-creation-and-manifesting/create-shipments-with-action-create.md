---
title: Create shipments with Create action
excerpt: >-
  Create is an action that initiates a new shipment entry in the system. This
  action captures all the necessary details of the shipment to generate shipping
  documents and prepare for the actual shipping process.
deprecated: false
hidden: false
icon: fad fa-cart-plus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

The **Create** action initiates a new shipment entry in the system without immediately generating a <Glossary>tracking number</Glossary>. This approach gives you more control over when tracking numbers are issued and labels are printed.

<Accordion title="Important: Label Printing and Manifesting" icon="exclamation-triangle">
You can only manifest the shipments for which you have printed the labels. Make sure to use the [Print Label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-rm-shipmentid) request before attempting to manifest your shipments.
</Accordion>

## How Create Action Works

<Cards columns={2}>
  <Card title="Delayed Tracking Numbers" icon="clock">
    Tracking numbers are not returned until you send the Print Label request, giving you flexibility in your shipping workflow.
  </Card>
  <Card title="Process Status Default" icon="cogs">
    If no action value is specified in the CreateShipment request, shipments are automatically created with "Process" status for backwards compatibility.
  </Card>
</Cards>

## Workflow Process

The Create action follows a specific workflow that separates shipment creation from label generation:

<Image align="center" alt="Example flow of creating shipment with Create action" border={false} caption="Workflow for creating shipments with Create action" src="https://files.readme.io/822c8b02ea907f91f7549757093ce56cf1c8823b6b310fe73a1b7874474bc8f1-Create_flow.png" />

<Columns layout="auto">
  <Column>
    ### Step-by-Step Process
    
    1. **Create Shipment**: Use the [CreateShipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) endpoint with Create action
    2. **Generate Labels**: Call the Print Label endpoint when ready
    3. **Manifest Shipments**: Process shipments for carrier pickup
  </Column>
  <Column>
    ### Benefits
    
    - **Flexible Timing**: Control when tracking numbers are generated
    - **Batch Processing**: Create multiple shipments before printing labels
    - **Error Prevention**: Verify shipment details before committing to labels
  </Column>
</Columns>

## Next Steps

Ready to implement the Create action workflow? Follow our comprehensive guide:

<TutorialTile emoji="🦉" slug="process-shipment-created-with-the-action-create" title="Process shipment created with the action &#x22;Create&#x22;" />

## Backwards Compatibility

This functionality maintains backwards compatibility to help existing customers migrate to the new platform seamlessly. Shipments without a specified action will automatically use the "Process" status.