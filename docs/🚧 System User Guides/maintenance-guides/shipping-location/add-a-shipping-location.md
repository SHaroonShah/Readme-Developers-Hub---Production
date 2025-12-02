---
title: Add Shipping Location
excerpt: >-
  A _shipping location_ is a physical address designated area from which the
  goods are sent or despatched. It plays a crucial role in the logistics and
  shipping process.
deprecated: false
hidden: false
icon: fad fa-location-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The process of adding a <Glossary>shipping location</Glossary> helps in streamlining the order fulfillment process, enhance inventory oversight, aids in coordination, and contributes to customer satisfaction. Shipping locations are fundamental to ensuring that the products are despatched effectively and reach their destinations in a timely manner.

To add a new shipping location in SAPIENT, follow the instructions as described in the following procedure.

<br />

<Tabs>
  <Tab title="Add via SAPIENT UI">
    <br />

    To add a shipping location in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping locations page</strong>} icon="fa-rocket">
        <br />

        From the SAPIENT **Home** page, in the left navigation panel, select **Shipping Locations**.

        <Image align="center" border={true} src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select add shipping location button</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Locations** page that appears, select ![alt text](https://files.readme.io/e50833cb14406497b4c50b5eb8c6997612af96e420fd9930bc45c1c883dd09a0-Add_shipping_location_button.png).

        <Image align="center" border={true} src="https://files.readme.io/6e836d0e0573bdc15c4d746439001e41ccf2631c0e7bb1bc2f38149dee53e9e3-Selecting_add_shipping_location_button.png" alt="Selecting option to add shipping location" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter location details </strong>} icon="fa-rocket">
        <br />

        On the **Add Shipping Location** form that opens, in the **LOCATION DETAILS** block, enter the necessary information.

        <Image align="center" border={true} src="https://files.readme.io/5e6bebc209c1497103efb0288fd1a0d15ddc0bbb04d07e5d7bc4490f825c649b-Location_details_block.png" alt="Entering location details" />

        <br />

        <AsteridkForMandatoryElements />

        | Element                              | Description                                                                                                                                                                                                         |
        | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        | **Name / Alias**\*                   | Enter the name of your location that you want to add.                                                                                                                                                               |
        | **Set As Default Shipping Location** | Turn on this toggle to set the location you entered as default. If you have previously set a <Glossary>default shipping location</Glossary>, then keeping this toggle off retains that location as the default one. |
        | **Time Zone**                        | From the dropdown menu, select the timezone which adheres to the location you are adding.                                                                                                                           |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter address details </strong>} icon="fa-rocket">
        <br />

        In the **ADDRESS DETAILS** block, enter the necessary information as shown below.

        <Image align="center" border={true} src="https://files.readme.io/3e977f9b76554494861e9900b8b9a42a8853cb4d2d4aa45c1042487dfbfd2380-Address_details_block.png" alt="Entering address details" />

        <br />

        <AsteridkForMandatoryElements />

        | Element            | Description                                                                                                                       |
        | ------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
        | **Country**\*      | Enter the name of the country where your location is based.                                                                       |
        | **Address**\*      | Enter the first line of address for your location.                                                                                |
        | **Address 2**      | Enter the second line of address for your location, if applicable.                                                                |
        | **Address 3**      | Enter the third line of address for your location, if applicable.                                                                 |
        | **Contact Number** | Enter the contact number that can be access at the location you are adding.                                                       |
        | **Town**\*         | Enter the name of the town where your location is based.                                                                          |
        | **County**         | Enter the name of the county where your location is based.                                                                        |
        | **Postcode**\*     | Enter the exact post code of the location you are adding.                                                                         |
        | **What3Words**     | Enter the <Glossary>What3words</Glossary> for your location to be able to get identified within the resolution of about 3 meters. |

        <br />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Finalise and save </strong>} icon="fa-rocket">
        <br />

        After entering all the relevant information, select ![alt text](https://files.readme.io/656f8ada261afe731847fa985571a318b7e27a15af1b7bb917149489b6f974ef-Add_shipping_location_button_2.png).

        Once done, a new shipping location is created successfully and appears in the **Shipping Locations** table. You can now manage it as per your business needs.

        <br />

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add via API">
    <br />

    To add a new shipping location via our API, refer to the following endpoint:

    <Cards>
      <Card title="Add Location" href="https://docs.intersoftsapient.net/reference/post_v4-shippinglocations#/" icon="fa-solid fa-code">
        Complete API reference for adding shipping location
      </Card>
    </Cards>
  </Tab>
</Tabs>

### See also

<Cards columns="3">
  <Card title="Edit Location" href="https://docs.intersoftsapient.net/docs/edit-shipping-location" icon="fa-solid fa-edit">
    Modify existing shipping location details and settings.
  </Card>

  <Card title="Link Location to Shipping Account" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="Fa- solid fa-link">
    Learn how to link a shipping location with an existing shipping account.
  </Card>

  <Card title="Delete Location" href="https://docs.intersoftsapient.net/docs/delete-shipping-location" icon="fa-solid fa-trash-alt">
    Remove shipping locations that are no longer needed.
  </Card>
</Cards>
