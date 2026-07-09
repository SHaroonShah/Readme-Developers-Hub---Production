---
title: Delete address
excerpt: >-
  Deleting an address involves removing an entry from the address book,
  typically when it is no longer needed or relevant.
deprecated: false
hidden: false
icon: fad fa-circle-trash
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can delete the address to keep the address book clean and manageable, ensuring that users are not overwhelmed by obsolete or unused entries. This also reduces the risk of errors by preventing confusion over which addresses are current and valid for shipping purposes.

## How to delete address

<Tabs>
  <Tab title="Delete via SAPIENT UI">
    

    To delete an address in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access address book</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Address Book**.

        <Image align="center" border={true} src="https://files.readme.io/145195adcbdbf39b1faea51d1afa71dcc10a408409060a05d02bc12fb48a8630-Address_option.png" alt="Accessing address book" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select address to delete</strong>} icon="fa-rocket">
        <br />

        In the **Address Book** page that opens, from the list, select the address that you want delete.

        <Image align="center" src="https://files.readme.io/ff8a355df4c747af6625d590d1ae4969c04ca1fc54583d44664f74dbaa97454d-Selecting_address_to_edit.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Delete address </strong>} icon="fa-rocket">
        <br />

        In the **Edit Address** form that opens, select ![](https://files.readme.io/e063903e72dbad4ea046d44cc7778b2228def2a4e7d8ff7ebde8655ca4c1db6f-Delete_address_button.png).

        <Image align="center" border={true} src="https://files.readme.io/8ee8a38d915dabaa307e82477eb90a872a81ca5652829bfc0be6d1a7f7a999b6-Delete_address_option.png" alt="Deleting address" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Confirm your action </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that opens, select **Yes** to confirm your action.

        <Image align="center" border={true} src="https://files.readme.io/4e31a217220e21a41f5bc9ba834c5b99372c54eeaccce8ca36a685f73f73fb68-Confirming_address_deletion.png" width="350px" alt="Confirming deletion" />

        <br />

        Once confirmed, the address is deleted from the system and no longer displayed in the **Address Book** list.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Delete via API">
    

    To delete an address via our API, refer to the following endpoint:

    <Cards>
      <Card title="Delete Address" href="https://docs.intersoftsapient.net/reference/delete_v4-addresses-addressid#/" icon="fa-solid fa-code">
        Complete API reference for deleting address from address book
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
</Cards>

<br />
