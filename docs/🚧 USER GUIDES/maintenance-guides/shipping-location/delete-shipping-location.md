---
title: Delete shipping location
excerpt: >-
  Learn how to delete shipping locations in SAPIENT through the UI or API when
  they are no longer required.
deprecated: false
hidden: false
icon: fad fa-location-xmark
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
Deleting a <Glossary>shipping location</Glossary> removes it from the system completely when it is no longer required.

<Accordion title="Why delete shipping locations?" icon="question-circle">
Deleting shipping locations could occur due to various reasons, such as:

* **Closure**: if a shipping facility is closed or no longer in use, deleting it helps avoid confusion in future shipping operations.
* **Account changes**: When a business relocates or decides to consolidate shipping operations to fewer locations.

In SAPIENT, you can delete the shipping location to keep the shipping database clean and manageable, preventing clutter from inactive or obsolete entries. It also improves the system performance and avoids potential confusion by ensuring only current and relevant shipping locations are available for selection or operation.
</Accordion>

## How to delete a shipping location

<Cards columns={2}>
  <Card title="Step 1: Navigate to Shipping Locations" icon="map-marker-alt">
    In the left navigation panel, select **Shipping Locations**.
    
    <Image align="center" alt="Accessing shipping locations" border={true} caption="Accessing shipping locations" src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" />
  </Card>
  
  <Card title="Step 2: Select and Edit Location" icon="edit">
    On the **Shipping Locations** page, select the shipping location you want to delete. On the **View Shipping Location [location name]** form that opens, select the edit button.
    
    <Image align="center" alt="Selecting option to add shipping location" border={true} caption="Selecting option to delete shipping location" src="https://files.readme.io/0ffbf35c04a6aa2b82329f91bca4df861fae2511cfbe07feeee4d9e97827d8c5-Edit_shippig_location_option.png" />
  </Card>
</Cards>

<Cards columns={2}>
  <Card title="Step 3: Delete the Location" icon="trash-alt">
    On the **Edit Shipping Location [location name]** form, select the delete button in the right corner.
    
    <Image align="center" alt="Entering location details" border={true} caption="Deleting shipping location" src="https://files.readme.io/bd3538aec38b70a7d69715426fca677ddc2922db2b942448fce828b6357e2cad-Deleting_shipping_location.png" />
  </Card>
  
  <Card title="Step 4: Confirm Deletion" icon="check-circle">
    In the confirmation dialog that appears, select **Yes** to confirm your action.
    
    <Image align="center" alt="Confirming deletion" border={true} caption="Confirming deletion" src="https://files.readme.io/a6e38fbaadee4529ebe22646e35a12534d4a944a8bfb768a243d02380f082af2-Confirming_account_deletion.png" width="350px" />
  </Card>
</Cards>

Once completed, the shipping location will be successfully deleted from the system.

<Accordion title="Alternative: Delete via API" icon="code">
Shipping locations can also be deleted via API. To learn more on how to delete your shipping locations via API, refer to the [API References](https://docs.intersoftsapient.net/reference/delete_v4-shippinglocations-shippinglocationid) section.
</Accordion>

## Related topics

<Cards>
  <Card title="Add shipping location" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="plus-circle">
    Learn how to create new shipping locations in SAPIENT
  </Card>
</Cards>