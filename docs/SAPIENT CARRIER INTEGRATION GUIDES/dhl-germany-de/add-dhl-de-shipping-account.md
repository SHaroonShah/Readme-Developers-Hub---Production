---
title: Add DHL DE shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-calendar-circle-plus
metadata:
  robots: index
---
In SAPIENT, with the Add Shipping Account functionality, you can select the desired shipping location and then add a DHL Germany shipping account to it.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have enabled the <Anchor label="label integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for DHL Germany._

## How to add DHL DE shipping account

To add a shipping account for DHL DE in SAPIENT, perform the steps as explained in the following procedure.

Expand each step to view the related instructions and field details.

<Tabs>
  <Tab title="Via SAPIENT UI">
    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" src="https://files.readme.io/3d2349061f0415b118f4ffc1d5d1f0722422302161528022cbc28634eb90514f-image.png" />
***
      </ToggleListItem>
<br />
      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png).

        <Image align="center" src="https://files.readme.io/a42649a2e896b24618507db2db02d7f7347225eabc56e04b4f79bcefea7c8ea8-image.png" />
***
      </ToggleListItem>
<br />
      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" src="https://files.readme.io/b7085aee7b1ca45c493a419c93c6866dac2426be296db4862aa890412013e36d-image.png" width="500px" />

        <AsteridkForMandatoryElements />

        | Element                 | Description                                                                                                   |
        | :---------------------- | :------------------------------------------------------------------------------------------------------------ |
        | **Carrier**\*           | From the dropdown list, select DHLDE -  DHL Germany.                                                          |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |
***
      </ToggleListItem>
<br />
      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/83810f18ee92f48d62b60191f940531365a413ee892f5fc77f3fd76772e24e87-image.png" width="400px" />

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
                **Carrier Account Number**\*
              </td>

              <td>
                Enter the unique 10-digit EKP (Einheitliche Kunden- und Produktnumme) number assigned by the DHL sales team.
              </td>
            </tr>

            <tr>
              <td>
                **Account Name (if different than customer)**\*
              </td>

              <td>
                Enter the name of the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Account Type**\*
              </td>

              <td>
                From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Alias**\*
              </td>

              <td>
                Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Name**\*
              </td>

              <td>
                Enter the contact name for the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Number**\*
              </td>

              <td>
                Enter the contact number for the account you are adding.
              </td>
            </tr>
          </tbody>
        </Table>
***
      </ToggleListItem>
<br />
      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" src="https://files.readme.io/0bd2bd4e7974be809da0cb97fda2d4f39e52d8177dbf53777bfa5ab3f0022b5f-image.png" width="450px" />

        <AsteridkForMandatoryElements />

        |           Element          | Description                                                                       |
        | :------------------------: | :-------------------------------------------------------------------------------- |
        | **DHL Germany Username**\* | Enter the unique identifier for the user account associated with DHL Germany.     |
        | **DHL Germany Password**\* | Enter the secure password used to authenticate the user account with DHL Germany. |
***
      </ToggleListItem>
<br />
      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png).

        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a DHL Germany shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dhlde" icon="fa-code">
        Add and manage DHL Germany shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={2}>
  <Card title="Edit shipping account" icon="fa-pen-to-square" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off">
    Update or modify an existing shipping account.
  </Card>
</Cards>

<br />
