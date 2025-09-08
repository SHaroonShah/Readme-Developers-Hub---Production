---
title: Add barcode range to YODEL shipping account
excerpt: >-
  A _barcode range_ is a specific set of numbers designated for tracking
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
The primary purpose of creating barcodes is to facilitate efficient tracking and management of shipments. Barcodes allow for the easy identification of items at various points in the shipping process, from dispatch to delivery. By assigning a unique barcode to each <Glossary>shipment</Glossary>, YODEL can streamline its operations and improve accuracy in handling processes.

The Yodel barcode is referred to as the License Plate Number, and is constructed as follows:​

* 8-digit prefix with a static value of static value of **JJD00022​**
* 11-digit tracking number, consisting of:​
  * 5-digit meter number​ provided during the [creation of the YODEL shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup-1#/). This number is variable and is used to automatically generate the barcode number range for the shipping account using that meter number.
  * 6-digit number range, always 00001 to 99999

> 🚧 _Important_
>
> _Before adding the barcode range, please be advised on the following:_
>
> * _The barcode range will only be auto-generated if a range does not already exist for that shipping account and meter number._
> * _The meter number must be unique and cannot be duplicated across shipping accounts._
> * _When the number range expires, Yodel issues a new meter number to the customer._

<br />
