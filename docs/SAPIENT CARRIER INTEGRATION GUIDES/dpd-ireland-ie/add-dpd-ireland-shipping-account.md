---
title: Add DPD Ireland shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, with the **Add Shipping Account** functionality, you can select the desired shipping location and then add a DPD Ireland shipping account to it.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have enabled the <Anchor label="label integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation">label integration</Anchor> for DHL Germany._

## How to add DPD Ireland shipping account

To add a shipping account for DPD Ireland in SAPIENT, perform the steps as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" caption="Accessing shipping accounts" src="https://files.readme.io/3d2349061f0415b118f4ffc1d5d1f0722422302161528022cbc28634eb90514f-image.png" />

2. On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png).

<Image align="center" caption="Selecting option to add shipping account" src="https://files.readme.io/a42649a2e896b24618507db2db02d7f7347225eabc56e04b4f79bcefea7c8ea8-image.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" width="550px" src="https://files.readme.io/86645219f87b869aff196c809ef6249918aa0e14533c668a9ac0b8be1f007cd9-image.png" />

<AsteridkForMandatoryElements />

| Element                | Description                                                                                                   |
| :--------------------- | :------------------------------------------------------------------------------------------------------------ |
| **Carrier***           | From the dropdown list, select **DPDIE -  DPD Ireland**.                                                      |
| **Shipping Location*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" width="500px" src="https://files.readme.io/c18989ccd749f6910c3f73b85cbf2bcca73358ef809018f03cfb226f78a6b82e-image.png" />

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
        **Carrier Account Number***
      </td>

      <td>
        Enter the carrier account number assigned to you by DPD Ireland.
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)***
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Alias***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

5. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" width="500px" src="https://files.readme.io/d4b4a30602ad21751b1cd1860976f17f00995d772dcbc15e817dde6c4188a483-image.png" />

<AsteridkForMandatoryElements />

|      Element     | Description                                                                                                                                                       |
| :--------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   **Username***  | Enter the username provided by DPD Ireland, used in API requests to authenticate the shipping account.                                                            |
|   **Password***  | Enter the password associated with the DPD Ireland account, used alongside the username for API authentication.                                                   |
| **Basic Token*** | Enter the secure authentication token provided by DPD Ireland, sent in the request header to support API authorisation; must be treated and stored as a password. |

6. After entering all the required information, select ![](https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png).

   Once done, you have now successfully added a shipping account. You can now start shipping with it.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dhlde)  section._

***

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)
