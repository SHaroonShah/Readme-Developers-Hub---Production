---
title: Add tracking barcode range to YODEL shipping account
excerpt: >-
  A tracking range_ is a specific set of numbers designated for tracking
  shipments. These barcodes are used to uniquely identify shipments at various
  stages of the shipping and handling process, facilitating efficient tracking
  and management.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The primary purpose of creating tracking barcode ranges is to facilitate efficient tracking and management of shipments. Barcodes allow for the easy identification of items at various points in the shipping process, from dispatch to delivery. By assigning a unique barcode to each <Glossary>shipment</Glossary>, YODEL can streamline its operations and improve accuracy in handling processes.

The Yodel barcode is referred to as the License Plate Number, and is constructed as follows:​

* 8-digit prefix with a static value of static value of **JJD00022​**
* 11-digit tracking number, consisting of:​
  * 5-digit meter number​ provided during the [creation of the YODEL shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup-1#/). This number is variable and is used to automatically generate the barcode number range for the shipping account using that meter number.
  * 6-digit number range, always 00001 to 99999

> 🚧 _Important_
>
> _Before adding the barcode range, please be advised on the following:_
>
> * _The barcode range will only be auto-generated if a range does not already exist for that <Glossary>shipping account</Glossary> and meter number._
> * _The meter number must be unique and cannot be duplicated across shipping accounts._
> * _When the number range expires, Yodel issues a new meter number to the customer to set up a new number range._

o add a barcode range for an An Post shipping account in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Integrations**.

<Image align="center" alt="Accessing integrations" border={true} caption="Accessing integrations" src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" />

2. In the list of carrier integrations that appears, next to YODEL, select **LABELS**.

<Image align="center" alt="Accessing labels integration" border={true} caption="Accessing labels integration" src="https://files.readme.io/ac19caa168fb20a2222372d76a597bb2356a9fa778755b67be518f99c0b301fa-Accessing_YODEL_label_integration.png" />

3. On the page that opens, under the **Available Integrations** block, in the **LABELS** section, select **CONFIGURE**.

<Image align="center" alt="Configuring labels integration" border={true} caption="Configuring labels integration" src="https://files.readme.io/929fcfc401a89d394d3c4cf236fa8aad9e1c300915efdf13c312ee009137e3f5-Configuring_YODEL_labels_integration.png" />

4. In the **Configure YODEL-** page that opens, select the **Tracking Ranges** tab and click ![](https://files.readme.io/9b441f42b92340c5b55aea80acf3097a095edd853fa67a58fd7e222cd5640c3d-Add_tracking_range_button.png).

<Image align="center" alt="Accessing option to add barcode range" border={true} caption="Accessing option to add barcode range" src="https://files.readme.io/50f00828730c4f0952268628bc6a78f253759fd809f059dcc682c6caeb7027cf-Selecting_add_tracking_range_for_YODEL.png" />

5. In the form that opens, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering barcode range details" border={true} caption="Entering barcode range details" src="https://files.readme.io/76f934376420cd8244640ffaa6f789563de4bfd4b9965f9c3fa03eec7d5cf59b-Adding_YODEL_tracking_range.png" />

<AsteridkForMandatoryElements />

|        Element        | Description                                                                                            |
| :-------------------: | :----------------------------------------------------------------------------------------------------- |
| **Shipping Account*** | From the dropdown menu, select the YODEL shipping account for which you are adding the tracking range. |
|       **Prefix**      | A read-only field that represents the YODEL's default prefix value.                                    |
|      **Range ***      | A read-only field that represents the YODEL's default 6-digit starting range value.                    |
|     **End Value***    | read-only field that represents the YODEL's default 6-digit ending range value.                        |

Once the relevant information is entered, select ![](https://files.readme.io/e5a8c301d9e4f9f09e3a21633bae40e536aaff09f96776a43aeea8162ece2a4b-Add_range_button.png) to save and add the tracking range for your shipping account range. You can now use this barcode range for your shipments.