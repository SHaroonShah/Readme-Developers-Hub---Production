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

|              Element              | Description                                                                                                                                                                                                                                                                                  |
| :-------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        **Customer Name\***        | Enter the name of the customer registered with FedEx.                                                                                                                                                                                                                                        |
|        **Address Line 1\***       | Enter the first line of the customer's address, typically including the street address or location where the customer is based. This is important for accurate delivery and communication.                                                                                                   |
|        **Address Line 2\***       | Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.                                                                                                            |
|        **Address Line 3\***       | Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.                                                                                                                                                                   |
|             **Town\***            | Enter the town or city where the customer is located.                                                                                                                                                                                                                                        |
|            **Country**            | Enter the country in which the customer resides.                                                                                                                                                                                                                                             |
|             **State**             | Enter the sate of the country where the customer is based.                                                                                                                                                                                                                                   |
|           **Postcode**\*          | Enter the postal/ZIP code for the customer's address.                                                                                                                                                                                                                                        |
| **This is a residential address** | Select this checkbox if the address provided is a residential address.                                                                                                                                                                                                                       |
|            **Previous**           | Select ![alt text](https://files.readme.io/32d1e0325bb43e32995a83a961895c700550d54e72e6ecdece1661a2fe88d0a9-Previous_button.png) to return to the [Shipping Account](https://docs.intersoftsapient.net/docs/specify-shipping-account-details#/) stage and update the information, if needed. |
|             **Submit**            | Select ![alt text](https://files.readme.io/d1aaa1a96df2bb864b3c2ff0bca425a2c21b8a8e159fa5bca06bdd323c0b3775-Submit_button.png) to save the entered information.                                                                                                                              |

Once the information is submitted, the system runs a validation check by validating the provided address via the**Address Validation** API. Based on the validation output, the system does the following:

* If the validation is successful, then the **accountAuthToken** is generated to be used in completing the multi-factor authentication process. Save the token and proceed to the Multi Factor Authentication stage of the form.

> 🚧 *Important*
>
> *The**accountAuthToken** is only valid for 30 minutes. If it is not utilised within this time period, then the shipping address is revalidated by triggering the **Address Validation** API to generate a new **accountAuthToken**.*

* If the validation fails (that is, the address is not matched in the FedEx systems), then a corresponding error message is displayed—and you will not proceed to the**Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form.