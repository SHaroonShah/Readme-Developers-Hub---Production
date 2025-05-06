---
title: Specify shipping address details (MFA stage 1)
excerpt: >-
  The Multi-Factor Authentication (MFA) is a two-step process that you need to
  follow when onboarding on a third-party software solution. The purpose is to
  validate your identity as a designated representative of the EAN-holding
  company whose account number is being used for onboarding. It has been
  introduced to avoid fraudulent activity.  
deprecated: false
hidden: true
metadata:
  robots: index
---
After [confirming the FedEx EULA](https://docs.intersoftsapient.net/docs/confirm-fedex-end-user-license-agreement#/), the **Shipping Address** stage is the first factor of authentication, where you can specify the shipping address details that are associated with the 9-digit FedEx account number, so that the system can validate and match it with the addresses stored in the FedEx system.

<Image align="center" className="border" border={true} src="https://files.readme.io/e0abd56eb4207f5e043cd1ba3259992715398fa85a2deaf011a014c8d02b85ca-FedEx_Shippig_address_stage.png" />

The information on how to fill in the the necessary information at this stage are explained in the following table.

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
        **Customer Name**\*
      </td>

      <td>
        Enter the name of the company or organisation registered with FedEx.
      </td>
    </tr>

    <tr>
      <td>
        **Country**\*
      </td>

      <td>
        From the dropdown menu, select the country in which the customer resides.
      </td>
    </tr>

    <tr>
      <td>
        **Address**\*
      </td>

      <td>
        Enter the first line of the customer's address, typically including the street address or location where the customer is based. This is important for accurate validation of the customer details.

        *`Note:`Make sure you enter the exact address that you have provided against your FedEx account number. If the address validation fails, you will not proceed to the**Multi-Factor Authentication** stage of the form.*
      </td>
    </tr>

    <tr>
      <td>
        **Address 2**\*
      </td>

      <td>
        Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.
      </td>
    </tr>

    <tr>
      <td>
        **Address 3**\*
      </td>

      <td>
        Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.
      </td>
    </tr>

    <tr>
      <td>
        **Town**\*
      </td>

      <td>
        Enter the town or city where the customer is located.
      </td>
    </tr>

    <tr>
      <td>
        **County**
      </td>

      <td>
        Enter the sate of the county where the customer is based.
      </td>
    </tr>

    <tr>
      <td>
        **Postcode**\*
      </td>

      <td>
        Enter the postal/ZIP code for the customer's address.
      </td>
    </tr>

    <tr>
      <td>
        **This is a residential address**
      </td>

      <td>
        Select this checkbox if the address provided is a residential address.
      </td>
    </tr>

    <tr>
      <td>
        **Previous**
      </td>

      <td>
        Select ![alt text](https://files.readme.io/32d1e0325bb43e32995a83a961895c700550d54e72e6ecdece1661a2fe88d0a9-Previous_button.png) to return to the [Shipping Account](https://docs.intersoftsapient.net/docs/specify-shipping-account-details#/) stage and update the information, if needed.
      </td>
    </tr>

    <tr>
      <td>
        **Submit**
      </td>

      <td>
        Select ![alt text](https://files.readme.io/d1aaa1a96df2bb864b3c2ff0bca425a2c21b8a8e159fa5bca06bdd323c0b3775-Submit_button.png) to save the entered information.
      </td>
    </tr>
  </tbody>
</Table>

Once the information is submitted, the system runs a validation check by validating the provided address via the**Address Validation** API. Based on the validation output, the system does the following:

* If the validation is successful, you can proceed to the [Multi Factor Authentication](https://docs.intersoftsapient.net/docs/initiate-multi-factoer-authentication-process#/) stage of the form.
* If the validation fails (that is, the address is not matched in the FedEx systems), then a corresponding error message is displayed—and you will not proceed to the **Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form. To proceed, you must correct the address details.