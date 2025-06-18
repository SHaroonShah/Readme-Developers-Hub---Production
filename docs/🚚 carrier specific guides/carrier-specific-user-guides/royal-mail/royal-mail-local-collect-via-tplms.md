---
title: Royal Mail Local Collect via TPLMS
deprecated: false
hidden: true
metadata:
  robots: index
---
> ❗️ *In development*
>
> *This feature is currently under development, once developed, this section will be moved to the**Use local collect shipment service** topic.*

## Use local collect with PUDO ID

Royal Mail’s Local Collect service is evolving to meet the needs of modern consumers. By enabling customers to receive their parcels at more diverse locations and providing a more robust data structure through the TPLMS file format, Royal Mail is enhancing the user experience and ensuring compliance with future shipping requirements

With the introduction of a new TPLMS file, Royal Mail now supports the following new additional location types while also updating the <Glossary>label</Glossary> and <Glossary>pre-advice</Glossary> file:

* **Lockers (LOK)**: Convenient parcel lockers available for pickup.
* **Collect+ Stores (PSH)**: A network of retail outlets, offering parcel collection services.

The following new fields have been introduced in the TPLMS file.

|             Field            | Description                                                                                                                         |
| :--------------------------: | :---------------------------------------------------------------------------------------------------------------------------------- |
|        **Supplier**\*        | Represents the name of the location supplier.                                                                                       |
|     **Supplement Code**\*    | Represents additional identification code for the location supplier.                                                                |
| **Supplier Location Type**\* | Represents the category of the supplier location, for example, Collect+.                                                            |
|        **Unique ID**\*       | Represents a distinct identifier for each collection point.                                                                         |
|        **Label ID**\*        | Represents a unique identifier associated with the shipment label.                                                                  |
|    **What3Words Value**\*    | Represents a precise address identifier for the location.                                                                           |
| **Final Collection Times**\* | Represents specified collection times for each day of the week.                                                                     |
|         **Products**         | Represents the list products accepted at the location.                                                                              |
|      **Max dimensions**      | Represents details regarding parcel size (small, medium, large) and weight limits for parcels that can be accepted at the location. |
|         **Signature**        | Represents whether the location accepts signature or non-signature shipments                                                        |
|         **Services**         | Represents the list of services offered at the location, for example, pick-up, drop-off, print label.                               |
|        **Facilities**        | Represents the information about the available facilities, for example, disabled access, indoor locker, car parking.                |
|  **Additional Information**  | Represents any additional information associated with the location.                                                                 |

Along with the new TPLMS file, the following new query parameters have been added to the Get PUDO Locations API request.

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
        **locationServices**
      </td>

      <td>
        This parameter specifies the available services offered at the PUDO location, such as pickup, dropoff, or print in store.
      </td>
    </tr>

    <tr>
      <td>
        **includeEnhancedLocationDetails**
      </td>

      <td>
        This parameter determines whether the response includes additional details about each PUDO location.

        • If set to true, the JSON response will include `enhancedLocationDetails` object for each PUDO location. This includes more comprehensive information, such as facilities available at the location, for example, disabled access, parking, and so on, distance from postcode, and any additional attributes relevant to the location that might insist customers in making informed decisions.

        • If set to false, the response will be limited to the basic details of the PUDO locations without the enhanced attributes.
      </td>
    </tr>
  </tbody>
</Table>

The following snippet represents an example JSON response schema of the Get PUDO Location endpoint via the TPLMS file.

```Text JSON
{
  "Locations": [
    {
      "CarrierCode": "RM",
      "LocationAlias": "J S Pound Plus",
      "LocationId": "2373391",
      "Address": {
        "Line1": "10 Grasmere Parade Wexham Road",
        "Line2": "",
        "Line3": "",
        "Town": "Slough",
        "Postcode": "SL2 5HZ",
        "Geolocation": {
          "Longitude": -0.5787,
          "Latitude": 51.5183
        },
        "OpeningHours": {
          "Monday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Tuesday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Wednesday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Thursday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Friday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Saturday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          },
          "Sunday": {
            "OpeningTime": "10:00:00",
            "ClosingTime": "21:00:00"
          }
        }
      },
      "enhancedLocationDetails": {
        "LocationType": "PSH",
        "Supplier": "Collect+",
        "SupplierLocationType": "Collect+",
        "LabelId": "31262463",
        "DistanceFromPostcode": "3.2",
		"DistanceUnit": "miles",
        "LocationAvailableFeatures": {
          "ServiceCode": "TPN|TPS|TPM|TPL|ITL|ITM|ITN|ITS|TRL|TRM|TRN|TRS|ITC|ITD|ITE|ITF",
          "AcceptSignature": "True",
          "AcceptNonSignature": "True",
          "LocationServices": "pickup|dropoff|printinstore",
          "Facilities": "carparking"
        },
        "LocationRestrictions": {
          "MaxHeight": "",
          "MaxWidth": "",
          "MaxLength": "",
          "MaxWeight": "",
          "MaxSize": ""
        }
      }
    }
  ],
  "TotalCount": 1
}
```

A new `PudoId` field is included in **Address** object of the Royal Mail Create Shipment request to recognise the specific Royal Mail location by its unique ID. When the `PudoId` field is utilised, the label and pre-advice will be generated with the updated information.

> 🚧 *Important*
>
> *Before providing the`pudoId`, make sure of the following:*
>
> * *For Royal Mail shipments,`pudoId` is only supported with the destination address (that is, collection shipments) as the Royal Mail's Local Collect label and pre-advice requirements only relate to this address. Please be advised that `pudoId` is not used for drop-off to a Local Collect store or Lockers as Royal Mail does not use the Unique ID for shipment drop-offs.*
> * *If the`pudoId` is provided for any other address other than the destination address, an error will be returned.*
> * *If the`pudoId` is provided for a carrier that does not use PUDO, an error will be returned.*
> * *If the destination company name includes “c/o” and the`PudoId` is not populated, the existing Local Collect functionality will continue to apply.*
> * Supplement code is automartically added to pre advice based on the Pudo ID