---
title: Add address
excerpt: >-
  Adding a new address involves including a new entry in the address book for a
  recipient, sender, or shipping location.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add as many addresses as you want to enhance the system's efficiency by allowing users to save frequently used addresses, reducing repetitive data entry during shipment creation. This process supports better organization of shipping logistics by easily categorising, accessing, and using multiple addresses in your <Glossary>shipment</Glossary> requests.

To add an address in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Address Book**.

<Image alt="Accessing address book" align="center" border={true} src="https://files.readme.io/145195adcbdbf39b1faea51d1afa71dcc10a408409060a05d02bc12fb48a8630-Address_option.png">
  Accessing address book
</Image>

2. In the **Address Book** page that opens, select ![alt text](https://files.readme.io/04fd0ca01e1aa046f9d359b1784c7829dfc49e228f54bd96c6929c86db7d79fa-Add_address_button.png).

<Image alt="Accessing option to add address" align="center" border={true} src="https://files.readme.io/8ae2dc77ad318b15a6820eafa0a2e377d27bdb399930a943b1234114ad63a4fc-Add_address_option.png">
  Accessing option to add address
</Image>

3. In the **Add Address** form that opens, in the **ADDRESS NAME** block, enter the **Address id** (your identifier for the address). 

> 📘 *Note*
>
> *If the Address id is not provided, then the system allocates one by default.*

<Image alt="Adding address name" align="center" width="400px" border={true} src="https://files.readme.io/023cc3556d6fb1c94f4a6342c6ec4bd549475a0e67cdde381a4aaa8fca5ac29a-Address_name_block.png">
  Adding address name
</Image>

4. Now, in the **ADDRESS DETAILS** block, enter the necessary information as explained in the following table.

<Image alt="Entering address details" align="center" border={true} src="https://files.readme.io/7c75448e34131d863e8b073a1c6afc592b7938e71b88744e044df22b9f7f1cf7-Address_details_block_2.png">
  Entering address details
</Image>

<AsteridkForMandatoryElements />

|       Element      | Description                                                                                                                       |
| :----------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
|  **Contact Name**  | Enter the name of the country where your location is based.                                                                       |
|    **Country\***   | From the dropdown menu, select the country code where the address you are adding is based.                                        |
|    **Address\***   | Enter the first line of address.                                                                                                  |
|    **Address 2**   | Enter the second line of address, if applicable.                                                                                  |
|    **Address 3**   | Enter the third line of address, if applicable.                                                                                   |
|  **Contact Email** | Enter the email address that can be accessed by the contact name provided.                                                        |
| **Contact Number** | Enter the contact number that can be accessed at the address you are adding.                                                      |
|  **Company Name**  | Enter the name of the company registered at the address you are adding.                                                           |
|     **Town\***     | Enter the name of the town where your address is based.                                                                           |
|     **County**     | Enter the name of the county where your address is based.                                                                         |
|   **Postcode\***   | Enter the exact postcode of the address you are adding.                                                                           |
|   **What3Words**   | Enter the  <Glossary>What3words</Glossary> for your address to be able to get identified within the resolution of about 3 meters. |

5. After entering the relevant information, select ![alt text](https://files.readme.io/e2e5dd875af649b5a87d4cbf536ab34d05d2123fe4b11ef132d8cb46ddd43e15-Add_address_button_2.png).

Once done, the address is added successfully and appears in the **Address Book** list.

> 📘 *Note*
>
> *Addresses can be added and managed via API. To learn more on how to add an address via API, refer to the[API References](https://docs.intersoftsapient.net/reference/post_v4-addresses) section.*
