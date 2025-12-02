---
title: Edit shipping location
excerpt: >-
  Editing a shipping location helps users maintain accurate and up-to-date
  shipping information, ensuring smooth operations and minimizing errors.
deprecated: false
hidden: false
icon: fad fa-location-pen
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can edit the <Glossary>shipping location</Glossary> to enhance customer service by providing the latest contact and operational details relevant to shipping activities.

<Tabs>
  <Tab title="Edit via SAPIENT UI">
    <br />

    To edit a shipping location in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping locations page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Locations**.

        <Image align="center" border={true} src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select location to edit</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Locations** page that appears, select the shipping location that you want to edit and on the **View Shipping Location\[location name]** form that opens, select the edit button ![alt text](https://files.readme.io/75c6ec5f5e8f7df63e70c61fec2bcf905b75de1822a4edbbd3d25ef5bd51b5ee-Edit_shippig_location_button.png).

        <Image align="center" border={true} src="https://files.readme.io/0ffbf35c04a6aa2b82329f91bca4df861fae2511cfbe07feeee4d9e97827d8c5-Edit_shippig_location_option.png" alt="Selecting option to add shipping location" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Update location details </strong>} icon="fa-rocket">
        <br />

        On the **Edit Shipping Location\[location name]** form that opens, update the necessary information as explained in the [Add shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) section.

        <Image align="center" border={true} src="https://files.readme.io/9cf3fcac3d841d769ecdc90e1f086dddda4bc04efcdc34618ad5f341309206bb-Editing_shipping_location.png" alt="Entering location details" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Save changes </strong>} icon="fa-rocket">
        <br />

        After entering all the relevant information, select the Save Changes button ![alt text](https://files.readme.io/5219ced5f0c085839c06983551f8930bbcb2c08eb4da69a39e36d59f4a5727c7-Save_changes_button.png).

        Once done, the shipping location is updated successfully.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Update via API">
    <br />

    To update a shipping location via our API, refer to the following endpoint:

    <Cards>
      <Card title="Update Location" href="https://docs.intersoftsapient.net/reference/put_v4-shippinglocations-shippinglocationid#/" icon="fa-solid fa-code">
        Complete API reference for updating shipping location
      </Card>
    </Cards>
  </Tab>
</Tabs>
