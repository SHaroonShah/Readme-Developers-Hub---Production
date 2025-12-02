---
title: Add Shipping Location
excerpt: >-
  Learn how to add shipping locations in SAPIENT to streamline order
  fulfillment, enhance inventory oversight, and improve customer satisfaction.
deprecated: false
hidden: false
icon: fad fa-location-plus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

The process of adding a <Glossary>shipping location</Glossary> helps in streamlining the order fulfillment process, enhance inventory oversight, aids in coordination, and contributes to customer satisfaction. Shipping locations are fundamental to ensuring that the products are despatched effectively and reach their destinations in a timely manner.

<Cards columns={2}>
  <Card title="Benefits" icon="check-circle">
    * Streamlined order fulfillment
    * Enhanced inventory oversight
    * Better coordination
    * Improved customer satisfaction
  </Card>

  <Card title="API Alternative" href="https://docs.intersoftsapient.net/reference/post_v4-shippinglocations" icon="code">
    Shipping locations can also be added and managed via API
  </Card>
</Cards>

## Step-by-Step Procedure

Follow these instructions to add a new shipping location in SAPIENT:

<Tabs>
  <Tab title="Getting Started">
    ### Step 1: Access SAPIENT

    Log in to the SAPIENT platform using your credentials.

    <Image align="center" border={true} src="https://files.readme.io/c2af709d6dafdead99cae2dfd707cdd74065a776db2a6ad1c641d28c2705d229-Sapient_Login_window.png" width="500px" />

    ### Step 2: Navigate to Shipping Locations

    From the SAPIENT **Home** page, in the left navigation panel, select **Shipping Locations**.

    <Image align="center" border={true} src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" alt="Accessing shipping locations" />

    ### Step 3: Initiate Adding Location

    On the **Shipping Locations** page that appears, select ![alt text](https://files.readme.io/e50833cb14406497b4c50b5eb8c6997612af96e420fd9930bc45c1c883dd09a0-Add_shipping_location_button.png).

    <Image align="center" border={true} src="https://files.readme.io/6e836d0e0573bdc15c4d746439001e41ccf2631c0e7bb1bc2f38149dee53e9e3-Selecting_add_shipping_location_button.png" alt="Selecting option to add shipping location" />
  </Tab>

  <Tab title="Location Details">
    ### Step 4: Configure Location Details

    On the **Add Shipping Location** form that opens, in the **LOCATION DETAILS** block, enter the necessary information.

    <Image align="center" border={true} src="https://files.readme.io/5e6bebc209c1497103efb0288fd1a0d15ddc0bbb04d07e5d7bc4490f825c649b-Location_details_block.png" alt="Entering location details" />

    <AsteridkForMandatoryElements />

    <Accordion title="Location Details Fields" icon="info-circle">
      | Element                              | Description                                                                                                                                                                                                         |
      | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
      | **Name / Alias**\*                   | Enter the name of your location that you want to add.                                                                                                                                                               |
      | **Set As Default Shipping Location** | Turn on this toggle to set the location you entered as default. If you have previously set a <Glossary>default shipping location</Glossary>, then keeping this toggle off retains that location as the default one. |
      | **Time Zone**                        | From the dropdown menu, select the timezone which adheres to the location you are adding.                                                                                                                           |
    </Accordion>
  </Tab>

  <Tab title="Address Details">
    ### Step 5: Enter Address Information

    In the **ADDRESS DETAILS** block, enter the necessary information as shown below.

    <Image align="center" border={true} src="https://files.readme.io/3e977f9b76554494861e9900b8b9a42a8853cb4d2d4aa45c1042487dfbfd2380-Address_details_block.png" alt="Entering address details" />

    <AsteridkForMandatoryElements />

    <Accordion title="Address Fields Reference" icon="map-marker-alt">
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
    </Accordion>
  </Tab>

  <Tab title="Complete Setup">
    ### Step 6: Finalize and Save

    After entering all the relevant information, select ![alt text](https://files.readme.io/656f8ada261afe731847fa985571a318b7e27a15af1b7bb917149489b6f974ef-Add_shipping_location_button_2.png).

    **Result:** Once done, a new shipping location is created successfully and appears in the **Shipping Locations** table. You can now manage it as per your business needs.

    > 📘 **Success!**
    >
    > Your new shipping location has been added to the system and is ready for use in your order fulfillment process.
  </Tab>
</Tabs>

## Next Steps

<Cards columns={3}>
  <Card title="Manage Locations" icon="cog">
    Configure and modify your existing shipping locations
  </Card>

  <Card title="API Integration" href="https://docs.intersoftsapient.net/reference/post_v4-shippinglocations" icon="plug">
    Explore API options for automated location management
  </Card>

  <Card title="Order Fulfillment" icon="truck">
    Start using your new shipping location for orders
  </Card>
</Cards>

> 📘 **Note**
>
> Shipping locations can be added and managed via API. To learn more on how to add shipping locations via API, refer to the [API References](https://docs.intersoftsapient.net/reference/post_v4-shippinglocations) section.
