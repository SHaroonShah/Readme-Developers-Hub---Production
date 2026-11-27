---
title: Combined label + CN22
excerpt: >-
  A combined label contains the shipping label and customs information on one
  label. This means you do not need to print a separate customs document.
deprecated: false
hidden: false
icon: fad fa-tachograph-digital
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
For eligible Royal Mail Import shipments with a total value of £135 or less, SAPIENT can generate a combined label that includes the Royal Mail shipping label and CN22 customs information on one 6x4 label.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _SAPIENT automatically determines whether a combined label + CN22 is generated based on the information provided in the Create Shipment request.<br />A combined label + CN22 is generated when all of the following conditions are met:_

  1. _You are a Royal Mail Freight 2 Post customer sending shipments from outside the UK to the UK._
  2. _The shipment contains no more than 8 items._
  3. _The total shipment value is £135 or less._
  4. _The requested label format is PDF._

  _If the shipment does not meet all of these requirements, SAPIENT will return a standard shipping label and a separate CN23 customs document in the Documents section of the Create Shipment response._

  _If the shipment value is provided in a currency other than GBP, SAPIENT automatically converts the value to GBP to determine which customs document is required._
</Callout>

The combined label can be used over a multiple range of services as explained in the following table:

| Service Code | Service Name                                |
| :----------: | :------------------------------------------ |
|    **DEA**   | DE Import Std 24 Parcel                     |
|    **DEB**   | DE Import RM24 Plus                         |
|    **DEC**   | DE Import Std 24 LLTR                       |
|    **DED**   | DE Import Std 48 LLTR                       |
|    **ITA**   | Import DE Tracked Returns 24                |
|    **ITB**   | Import DE Tracked Returns 48                |
|    **ITC**   | Import DE Crossborder Tracked 24 (LBT) (HV) |
|    **ITE**   | Import DE Crossborder Tracked 48 (LBT) (HV) |
|    **ITF**   | Import DE Crossborder Tracked 24 (LBT)      |
|    **ITL**   | Import DE Tracked 48 Parcels                |
|    **ITM**   | Import DE Tracked 24 Parcels                |
|    **ITN**   | Import DE Tracked 24- With Signature        |
|    **ITS**   | Import DE Tracked 48 - Non Signature        |
|    **DEP**   | DEImpUK Std24 PCL (WH)                      |
|    **DEQ**   | DEImpUK Std24 LLTR (WH)                     |
|    **DER**   | DEImpUK Std48 LLTR (WH)                     |
|    **DEU**   | DEImpUK Trk48 PCL (BOX)(HV)(WH)             |
|    **DEV**   | DEImpUK Trk48 PCL (BOX)(HV)(WH)             |
|    **DEX**   | DEImpUK Trk48 PCL (BOX)(WH)                 |
|    **DEY**   | DEImpUK Trk24 PCL (BOX)(WH)                 |
|    **DEZ**   | DEImpUK Trk48 PCL (TPL)(WH)                 |
|    **DE5**   | DEImpUK Trk24 PCL (TPM)(WH)                 |
|    **DE9**   | DEImpUK Trk48 PCL (AGE)(HV)                 |
|    **DE7**   | DEImpUK Trk24 PCL (AGE)(HV)(WH)             |
|    **DE8**   | DEImpUK Trk48 PCL (AGE)(HV)(WH)             |
|    **ITI**   | Import DE Tracked 24 Std Age                |
|    **ITJ**   | Import DE Tracked 24 THV Age                |

For customers and businesses using Royal Mail for their shipping needs, this combined label offers a more efficient process, simplifying documentation and tracking for lower-value shipments. It is crucial to stay informed about this update and to prepare for the necessary adjustments in operations to accommodate the new label format.


<Image src="https://files.readme.io/28e12fbd3aa096410869143a313b58e10f2682a1d96999f7c837e0148bde8d61-Combined_Label_and_CN22_sample.png" alt="Combined label example" align="center" width="500px" caption="Combined label + CN22 example" border={true} />


<br />


<Image src="https://files.readme.io/99c8343374d14f7e27598d5e1b16c081841819f76bd7b8b8242359a640cf8a1e-image.png" align="center" caption="CN23 documentation example" border={true} />

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the&#x20;_**_Sign & Date_**_&#x20;section of  the combined label, you can use your own signature or logo if you have&#x20;_[added and configured it](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/)_&#x20;via the SAPIENT UI. If the signature and logo has not been configured, then by default, the Shipper Contact Name is used._
</Callout>