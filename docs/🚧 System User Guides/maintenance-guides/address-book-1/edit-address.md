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
  <Tab title="Edit via SAPIENT UI">
    <br />

    To edit an address in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access address book</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Address Book**.

        <Image align="center" border={true} src="https://files.readme.io/145195adcbdbf39b1faea51d1afa71dcc10a408409060a05d02bc12fb48a8630-Address_option.png" alt="Accessing address book" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select address to edit</strong>} icon="fa-rocket">
        <br />

        In the **Address Book** page that opens, from the list, select the address that you want edit.

        <Image align="center" src="https://files.readme.io/ff8a355df4c747af6625d590d1ae4969c04ca1fc54583d44664f74dbaa97454d-Selecting_address_to_edit.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Edit address </strong>} icon="fa-rocket">
        <br />

        In the **Edit Address** form that opens, update the necessary information as explained in the [Add address](https://docs.intersoftsapient.net/docs/add-address#/) section.

        <Image align="center" border={true} src="https://files.readme.io/1b3e80e0f16f5a38056c1e8fa5a41a42ce78f1012f724c2eaa3075a366de6b85-Editing_address.png" alt="Editing address" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Save your changes </strong>} icon="fa-rocket">
        <br />

        After updating the relevant information, select ![](https://files.readme.io/ad9e5914fc6e05f9f14e1da660f4d564a88845b37bfe08a5efbf76997ebb406a-Save_changes_button.png).

        Once done, the address is updated successfully and now up-to-date.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Edit via API">
    <br />

    To edit an address via our API, refer to the following endpoint:

    <Cards>
      <Card title="Update Address Book" href="https://docs.intersoftsapient.net/reference/put_v4-addresses-addressid#/" icon="fa-solid fa-code">
        Complete API reference for editing address in address book
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards>
  <Card title="Add Address" href="https://docs.intersoftsapient.net/docs/add-address" icon="fa-solid fa-plus-circle">
    Create new addresses for customers, vendors, suppliers, or warehouse locations to expand your address repository.
  </Card>

  <Card title="Delete Address" href="https://docs.intersoftsapient.net/docs/delete-address" icon="fa-solid fa-trash">
    Remove outdated or unnecessary addresses to maintain a clean and organised address book.
  </Card>
</Cards>
