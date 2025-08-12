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

1. Log in to the SAPIENT platform using your credentials.

<Image align="center" className="border" border={true} width="500px" src="https://files.readme.io/c2af709d6dafdead99cae2dfd707cdd74065a776db2a6ad1c641d28c2705d229-Sapient_Login_window.png" />

2. On the **Home** page that opens, in the left navigation panel, select **Shipping Locations**.

<Image align="center" alt="Accessing shipping locations" border={true} caption="Accessing shipping locations" src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" />

3. On the **Shipping Locations** page that appears, select ![alt text](https://files.readme.io/e50833cb14406497b4c50b5eb8c6997612af96e420fd9930bc45c1c883dd09a0-Add_shipping_location_button.png).

<Image align="center" alt="Selecting option to add shipping location" border={true} caption="Selecting option to add shipping location" src="https://files.readme.io/6e836d0e0573bdc15c4d746439001e41ccf2631c0e7bb1bc2f38149dee53e9e3-Selecting_add_shipping_location_button.png" />

4. On the **Add Shipping Location** form that opens, in the **LOCATION DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering location details" border={true} caption="Entering location details" src="https://files.readme.io/5e6bebc209c1497103efb0288fd1a0d15ddc0bbb04d07e5d7bc4490f825c649b-Location_details_block.png" />

<AsteridkForMandatoryElements />

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
        **Name / Alias**\*
      </td>

      <td>
        Enter the name of your location that you want to add.
      </td>
    </tr>

    <tr>
      <td>
        **Set As Default Shipping Location**
      </td>

      <td>
        Turn on this toggle to set the location you entered as default.

        If you have previously set a <Glossary>default shipping location</Glossary>, then keeping this toggle off retains that location as the default one.
      </td>
    </tr>

    <tr>
      <td>
        **Time Zone**
      </td>

      <td>
        From the dropdown menu, select the timezone which adheres to the location you are adding.
      </td>
    </tr>
  </tbody>
</Table>

5. Now, in the **ADDRESS DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering address details" border={true} caption="Entering address details" src="https://files.readme.io/3e977f9b76554494861e9900b8b9a42a8853cb4d2d4aa45c1042487dfbfd2380-Address_details_block.png" />

<AsteridkForMandatoryElements />

|       Element      | Description                                                                                                                        |
| :----------------: | :--------------------------------------------------------------------------------------------------------------------------------- |
|    **Country**\*   | Enter the name of the country where your location is based.                                                                        |
|    **Address**\*   | Enter the first line of address for your location.                                                                                 |
|    **Address 2**   | Enter the second line of address for your location, if applicable.                                                                 |
|    **Address 3**   | Enter the third line of address for your location, if applicable.                                                                  |
| **Contact Number** | Enter the contact number that can be access at the location you are adding.                                                        |
|     **Town**\*     | Enter the name of the town where your location is based.                                                                           |
|     **County**     | Enter the name of the county where your location is based.                                                                         |
|   **Postcode**\*   | Enter the exact post code of the location you are adding.                                                                          |
|   **What3Words**   | Enter the  <Glossary>What3words</Glossary> for your location to be able to get identified within the resolution of about 3 meters. |

6. After entering all the relevant information, select ![alt text](https://files.readme.io/656f8ada261afe731847fa985571a318b7e27a15af1b7bb917149489b6f974ef-Add_shipping_location_button_2.png).

Once done, a new shipping location is created successfully and appears in the **Shipping Locations** table. You can now manage it as per your business needs.

> 📘 *Note*
>
> *Shipping locations can be added and managed via API. To learn more on how to add a shipping locations via API, refer to the [API References](https://docs.intersoftsapient.net/reference/post_v4-shippinglocations) section.*