---
title: Specify shipping address details
deprecated: false
hidden: true
metadata:
  robots: index
---
After defining the shipping account details, at the **Shipping Address** stage, you can specify the shipping address details so that the system can validate and match it with the addresses stored in the FedEx system.

> 🚧 *Important*
>
> *Make sure to provide the the exact shipping address, as this information is validated via the**Address Validation** API. If the address does not match, then a corresponding error message is displayed—and you will not proceed to the**Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form.*

<Image align="center" src="https://files.readme.io/ad642e851f763c932704c009f09f8e7b80479d4789161cd69b26396fabea4733-FedEx_Shippig_address_stage.png" />

The information on how to fill in the the necessary information at this stage are explained in the following table.

<AsteridkForMandatoryElements />

<br />

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
        **Customer Name\***
      </td>

      <td>
        Enter the name of the customer that
      </td>
    </tr>

    <tr>
      <td>
        **Address Line 1\***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Address Line 2\***
      </td>

      <td>
        Enter the account name.
      </td>
    </tr>

    <tr>
      <td>
        **Registered Email Address\***
      </td>

      <td>
        Enter the email address that was used to register the account for the carrier you selected.
      </td>
    </tr>

    <tr>
      <td>
        **Address Line 3\***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping location ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Town\***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Country\***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **State**
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Postcode**
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **This is a residential address**
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Previous**
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Submit**
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>