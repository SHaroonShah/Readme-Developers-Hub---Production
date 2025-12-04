---
title: Add address
excerpt: >-
  Adding a new address involves including a new entry in the address book for a
  recipient, sender, or shipping location.
deprecated: false
hidden: false
icon: fad fa-book-medical
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add as many addresses as you want to enhance the system's efficiency by allowing users to save frequently used addresses, reducing repetitive data entry during shipment creation. This process supports better organization of shipping logistics by easily categorising, accessing, and using multiple addresses in your <Glossary>shipment</Glossary> requests.

##

<Tabs>
  <Tab title="Add via SAPIENT UI">
    <br />

    To add an address to the address book in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access address book</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Address Book**.

    <Image align="center" border={true} src="https://files.readme.io/145195adcbdbf39b1faea51d1afa71dcc10a408409060a05d02bc12fb48a8630-Address_option.png" alt="Accessing address book" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select option to add address</strong>} icon="fa-rocket">
        <br />

         In the **Address Book** page that opens, select ![alt text](https://files.readme.io/04fd0ca01e1aa046f9d359b1784c7829dfc49e228f54bd96c6929c86db7d79fa-Add_address_button.png).

    <Image align="center" border={true} src="https://files.readme.io/8ae2dc77ad318b15a6820eafa0a2e377d27bdb399930a943b1234114ad63a4fc-Add_address_option.png" alt="Accessing option to add address" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter address ID </strong>} icon="fa-rocket">
        <br />

        In the **Add Address** form that opens, in the **ADDRESS NAME** block, enter the **Address id** (your identifier for the address).

    > 📘 *Note*
    >
    > *If the Address id is not provided, then the system allocates one by default.*

    <Image align="center" border={true} src="https://files.readme.io/023cc3556d6fb1c94f4a6342c6ec4bd549475a0e67cdde381a4aaa8fca5ac29a-Address_name_block.png" width="400px" alt="Adding address name" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter complete address details </strong>} icon="fa-rocket">
        <br />

         In the **ADDRESS DETAILS** block, enter the necessary information according to the field descriptions below.

    <Image align="center" border={true} src="https://files.readme.io/7c75448e34131d863e8b073a1c6afc592b7938e71b88744e044df22b9f7f1cf7-Address_details_block_2.png" alt="Entering address details" /><br />

      <AsteridkForMandatoryElements />

      |       Element      | Description                                                                                                                       |
      | :----------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
      |  **Contact Name**  | Enter the name of the country where your location is based.                                                                       |
      |    **Country**\*   | From the dropdown menu, select the country code where the address you are adding is based.                                        |
      |    **Address**\*   | Enter the first line of address.                                                                                                  |
      |    **Address 2**   | Enter the second line of address, if applicable.                                                                                  |
      |    **Address 3**   | Enter the third line of address, if applicable.                                                                                   |
      |  **Contact Email** | Enter the email address that can be accessed by the contact name provided.                                                        |
      | **Contact Number** | Enter the contact number that can be accessed at the address you are adding.                                                      |
      |  **Company Name**  | Enter the name of the company registered at the address you are adding.                                                           |
      |     **Town**\*     | Enter the name of the town where your address is based.                                                                           |
      |     **County**     | Enter the name of the county where your address is based.                                                                         |
      |   **Postcode**\*   | Enter the exact postcode of the address you are adding.                                                                           |
      |   **What3Words**   | Enter the  <Glossary>What3words</Glossary> for your address to be able to get identified within the resolution of about 3 meters. |
    ***
      </ToggleListItem><br />
<ToggleListItem title={<strong>5. Save the address </strong>} icon="fa-rocket">
        <br />

        After entering the relevant information, select ![alt text](https://files.readme.io/e2e5dd875af649b5a87d4cbf536ab34d05d2123fe4b11ef132d8cb46ddd43e15-Add_address_button_2.png).

    Once completed, the address is added successfully and appears in the **Address Book** list.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add via API">
    <br />

    To add an address to the address book via our API, refer to the following endpoint:

    <Cards>
      <Card title="Add Address" href="https://docs.intersoftsapient.net/reference/post_v4-addresses#/" icon="fa-solid fa-code">
        Complete API reference for adding address to address book
      </Card>
    </Cards>
  </Tab>
</Tabs>
