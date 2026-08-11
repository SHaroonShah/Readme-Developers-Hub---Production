---
title: Delete shipping location
excerpt: >-
  Deleting a shipping location means removing it from the system completely when
  it is no longer required.
deprecated: false
hidden: false
icon: fad fa-location-xmark
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Deleting the <Glossary>shipping location</Glossary> could occur due to various reasons, such as:

* **Closure**: if a shipping facility is closed or no longer in use, deleting it helps avoid confusion in future shipping operations.
* **Account changes**: When a business relocates or decides to consolidate shipping operations to fewer locations.

In SAPIENT, you can delete the shipping location to keep the shipping database clean and manageable, preventing clutter from inactive or obsolete entries. It also improves the system performance and avoids potential confusion by ensuring only current and relevant shipping locations are available for selection or operation.

## How to delete shipping location

<Tabs>
  <Tab title="Delete via SAPIENT UI">
    

    To delete a shipping location in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping locations page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Locations**.

        <Image align="center" border={true} src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" caption="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select location to delete</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Locations** page, select the shipping location you want to delete. On the **View Shipping Location \[location name]** form that opens, select the **Edit Shipping Location** button.

        <Image align="center" border={true} src="https://files.readme.io/0ffbf35c04a6aa2b82329f91bca4df861fae2511cfbe07feeee4d9e97827d8c5-Edit_shippig_location_option.png" caption="Selecting option to edit shipping location" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Delete location </strong>} icon="fa-rocket">
        <br />

        On the **Edit Shipping Location \[location name]** form, select the delete button in the right corner.

        <Image align="center" border={true} src="https://files.readme.io/bd3538aec38b70a7d69715426fca677ddc2922db2b942448fce828b6357e2cad-Deleting_shipping_location.png" caption="Deleting location details" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Confirm deletion </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, select **Yes** to confirm your action.

        <Image align="center" border={true} src="https://files.readme.io/a6e38fbaadee4529ebe22646e35a12534d4a944a8bfb768a243d02380f082af2-Confirming_account_deletion.png" width="350px" caption="Confirming deletion" />
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Edit via API">
    

    To delete a shipping location via our API, refer to the following endpoint:

    <Cards>
      <Card title="Delete Location" href="https://docs.intersoftsapient.net/v4.04/reference/delete_v4-shippinglocations-shippinglocationid#/" icon="fa-solid fa-code">
        Complete API reference for deleting shipping location
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards>
  <Card title="Add shipping location" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="fa-solid fa-plus-circle">
    Learn how to create new shipping locations in SAPIENT
  </Card>
</Cards>