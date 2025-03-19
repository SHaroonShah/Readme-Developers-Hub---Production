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

|              Element              | Description                                                                                                                                                                                |
| :-------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        **Customer Name\***        | Enter the name of the customer registered with FedEx.                                                                                                                                      |
|        **Address Line 1\***       | Enter the first line of the customer's address, typically including the street address or location where the customer is based. This is important for accurate delivery and communication. |
|        **Address Line 2\***       | Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.          |
|        **Address Line 3\***       | Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.                                                                 |
|             **Town\***            | Enter the town or city where the customer is located.                                                                                                                                      |
|           **Country\***           | Enter the country in which the customer resides.                                                                                                                                           |
|             **State**             | Enter the sate of the country where the customer is based.                                                                                                                                 |
|            **Postcode**           |                                                                                                                                                                                            |
| **This is a residential address** |                                                                                                                                                                                            |
|            **Previous**           |                                                                                                                                                                                            |
|             **Submit**            |                                                                                                                                                                                            |