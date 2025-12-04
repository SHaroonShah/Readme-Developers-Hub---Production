---
title: Edit address
excerpt: >-
  Editing an address allows users to update or correct existing address
  information, such as street names, postal codes, or contact details.
deprecated: false
hidden: false
icon: fad fa-square-pen
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can edit the addresses that you have added previously to maintain accuracy in the shipping data, which is crucial for ensuring timely and correct deliveries. It also helps in reducing shipping errors that could arise from outdated or incorrect address information.

## How to edit address

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

        In the **ADDRESS DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/7c75448e34131d863e8b073a1c6afc592b7938e71b88744e044df22b9f7f1cf7-Address_details_block_2.png" alt="Entering address details" />

        <br />

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
      </ToggleListItem>

      <br />

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

To edit an address in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Address Book**.

<Image align="center" alt="Accessing address book" border={true} caption="Accessing address book" src="https://files.readme.io/145195adcbdbf39b1faea51d1afa71dcc10a408409060a05d02bc12fb48a8630-Address_option.png" />

2. In the **Address Book** page that opens, from the list, select the address that you want edit.

<Image align="center" alt="Accessing option to add address" border={true} caption="Editing address" src="https://files.readme.io/4eb2b8b120c2894a1c42c57b7ab17d508d933c2de59520bd5be2f88b08f723f8-Editing_address.png" />

3. In the **Edit Address** form that opens, update the necessary information as explained in the Add address section.

<Image align="center" alt="Editing address" border={true} caption="Editing address" src="https://files.readme.io/1b3e80e0f16f5a38056c1e8fa5a41a42ce78f1012f724c2eaa3075a366de6b85-Editing_address.png" />

4. After updating the relevant information, select ![](https://files.readme.io/ad9e5914fc6e05f9f14e1da660f4d564a88845b37bfe08a5efbf76997ebb406a-Save_changes_button.png).

Once done, the address is updated successfully and now up-to-date.

> 📘 _Note_
>
> _Addresses can be modified via API. To learn more on how to edit an address via API, refer to the [API References](https://docs.intersoftsapient.net/reference/put_v4-addresses-addressid) section._
