---
title: Use PUDO service
excerpt: >-
  The Royal Mail Pick Up and Drop Off (PUDO) service enables customers to use a
  convenient out of home option to collect or return parcels at designated
  locations. These locations can include Post Offices, retail stores, or
  lockers, offering greater convenience and flexibility for customers. 
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The [PUDO API](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) enhances customer convenience by allowing them to access essential shipping options for both sending and returning packages seamlessly by offering the following options:

* **Pick Up**: Allows customers to choose to collect their parcel from a PUDO point. It is particularly beneficial for those who may not always be available for direct delivery, helping to reduce missed delivery attempts and enhance overall customer satisfaction.
* **Drop-off**: Allows customers to find a location where they can drop off a parcel they want to return.

<Image align="center" className="border" border={true} width="200px" src="https://files.readme.io/fc9948cba5b87c15e89ceda1d55fe6f022a938bb2b8661ace1f6f9c9e5572799-Post_office.gif" />

With the advancements in the location services, Royal Mail now supports the following location types:

📍**Customer Service point (CSP)**: Customer Service Point at a Delivery Office.

📍**Post Office (POL)**: Nearby post office.

📍**Lockers (LOK)**: Convenient parcel lockers available for pickup.

📍**Collect+ Stores (PSH)**: A network of retail outlets, offering parcel collection services.

The SAPIENT system offers two effective approaches for accessing PUDO (Pick Up Drop Off) locations to enhance local collection options for Royal Mail customers.

The first method utilises the [PUDO API](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/), which allows users to retrieve nearby collection points on an ad-hoc basis during checkout ensuring real-time access to essential location information.

The second approach involves SFTP (Secure File Transfer Protocol), where customers can download a comprehensive, daily-updated library of all available PUDO locations.

Together, these options provide flexibility and convenience, catering to the diverse shipping needs of Royal Mail customers.

Based on your requirements, you can choose various approaches to use the PUDO lookup and create a Royal Mail shipment with the Local Collect enhancement as explained in the following sections.

<Accordion title="Utilising PUDO API for local collect">
  In the SAPIENT system, the integration of the PUDO API allows Royal Mail customers to efficiently access collection point locations for their shipments. This API is a vital component of the local collect enhancement, offering a flexible solution during the checkout process.

  ## How it works

  1. **Integration Activation**: The PUDO integration must be enabled within the Sapient system for customers to leverage this feature.

  <Image align="center" border={true} src="https://files.readme.io/130681c4ccc5018415e332ba70d3239a8e6c5b1c30b509fd21437710dfe3c46a-image.png" />

  2. **Ad-Hoc Calling**: During the checkout process, customers can call the PUDO API to retrieve a list of nearby collection points based on their delivery address.
  3. **Result Delivery**: The API responds with a real-time list of PUDO locations for selection.

  The following new query parameters have been added to the [Get PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) API request.

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

  The following snippet represents an example JSON response schema of the Get PUDO Location endpoint.

  ```
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
</Accordion>

<Accordion title="Accessing PUDO Locations via SFTP for local collect">
  The PUDO SFTP (Secure File Transfer Protocol) integration involves establishing a secure connection that enables data exchange between you and Intersoft. This integration facilitates the exchange of crucial information, such as drop-off locations, opening and closing times, and shipment tracking details in a secure manner.

  ## How it works

  You can use the SFTP solution, if you want to download the PUDO data into your own system to check the PUDO locations that are close by to a given address by yourself.

  > 🚧 *Important*
  >
  > *If you want to set up the PUDO integration, make sure to meet the following prerequisites:*
  >
  > *[Enable PUDO integration](https://docs.intersoftsapient.net/v4.02_Archive/update/docs/integration-activation#/) via the Royal Mail Integration Activation screen.*
  >
  >   <Image align="center" src="https://files.readme.io/735e213c58d29db4438e9cc89a873cba9c4a35bbaaf4f3663f68817f8c32327a-image.png" />
  >
  > *[Raise a request](mailto:onboarding@intersoftsapient.net) to our onboarding team to create a location for you to connect and download the PUDO data via SFTP by providing your RSA Public Key through a secure gateway. Our team will respond with your connection details.*

  The PUDO SFTP solution provides you with all locations in a single file that you can store as a library.

  > 💡 *Tip*
  >
  > *The file is generated on a daily basis. To learn more about the file structure and its data, refer to the following example file:*
  >
  > * [RMPUDO20250619](https://docs.google.com/spreadsheets/d/1DZ1INbGf893MCEF1ijgeMOZn-cskd0TDcZW7DtPJjLQ/edit?usp=sharing)
  >
  > *This file is available for download on a daily basis via SFTP. You must first connect to the location, download the file, and then close the connection. You cannot delete or move the file, you can only download it.*
</Accordion>

<Accordion title="Create shipment using local collect enhancement">
  In SAPIENT, there are two distinct ways to [create a Royal Mail shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) aimed at delivery to a PUDO point—one method involves using the direct address of the chosen location, while the other relies on utilising the `pudoId` returned from the PUDO lookup, offering flexibility in how shipments can be generated.

  To make the **LocalCollect** shipment request, it is necessary to provide the following information:

  1. The request must include *“c/o”* with the location name.
  2. The **ServiceEnhancements** code—**LocalCollect** must be used.
  3. The **Email** or **SMS** notification service enhancement must be used by providing the destination's **ContactPhone** or **ContactEmail** information, so the end consumer can be notified when their item is ready to be collected from the post office.

  Keeping intact the existing functionality, for a more enhanced user experience, new `pudoId` field is included in **Address** object of the Royal Mail Create Shipment request to recognise the specific Royal Mail location by its unique ID. When the `pudoId` field is utilised, the label and pre-advice will be generated with the updated information.

  > 🚧 *Important*
  >
  > *Before providing the`pudoId`, make sure of the following:*
  >
  > * *For Royal Mail shipments,`pudoId` is only supported with the destination address (that is, an outbound shipment for a delivery to a PUDO location) as the Royal Mail's Local Collect label requirements only relate to this address. Please be advised that `pudoId` is not used for drop-off to a Local Collect store or Lockers as Royal Mail does not use the Unique ID for shipment drop-offs.*
  > * *If the`pudoId` is provided for any other address other than the destination address, an error will be returned.*
  > * *If the`pudoId` is provided for a carrier that does not use PUDO, an error will be returned.*
  > * *If the destination company name includes “c/o” and the`PudoId` is not populated, the existing Local Collect functionality will continue to apply.*
</Accordion>