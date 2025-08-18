---
title: Royal Mail Parcel Force services
excerpt: >-
  Royal Mail has taken significant steps to enhance its operations by
  replicating the existing Parcelforce’s international and domestic services
  into their own software systems. This is done to expand the operational
  software capabilities within the Royal Mail Group, thereby streamlining
  operations within the Royal Mail network.
deprecated: false
hidden: true
icon: fad fa-square-dashed-circle-plus
metadata:
  robots: index
---
The introduction of the new services represents a comprehensive approach to international and domestic shipping needs. Some international services require a partner label for completing the final mile delivery.

A *partner label* is a shipping label utilised in collaboration with other carriers, which facilitates the last-mile delivery of shipments. For Royal Mail, partners such as GLS and FedEx will use these partner labels to manage the final stages of delivery to the recipient outside the UK.

Partner label involves utilising two separate labels on a shipment to reflect both the originating carrier (Royal Mail) and the partner carrier (GLS or FedEx) responsible for the last-mile delivery. Therefore, for services using partner labels, SAPIENT will generate both the Royal Mail and partner label and return them in the Create Shipment response. This dual labelling mechanism helps streamline the logistics process and enhances tracking and accountability throughout the delivery journey. By utilising partners, Royal Mail aims to provide an enhanced service that meets customer expectations around the globe.

<Accordion title="International Services">
  The new Royal Mail international services are listed in the following table.

  | Service Code | Service Name                     | Partner Label Required | Partner Carrier |
  | :----------: | :------------------------------- | :--------------------- | :-------------- |
  |      ERB     | EUROPRIORITY DDP                 | ✅                      | GLS             |
  |      ER6     | EUROPRIORITY DDP-EXTRACOMP1      | ✅                      | GLS             |
  |      ER7     | EUROPRIORITY DDP-EXTRACOMP2      | ✅                      | GLS             |
  |      ER8     | EUROPRIORITY DDP-EXTRACOMP3      | ✅                      | GLS             |
  |      ERA     | EUROPRIORITY DTP IOSS            | ✅                      | GLS             |
  |      ER1     | EUROPRIORITY DTP IOSS-EXTRACOMP1 | ✅                      | GLS             |
  |      ER2     | EUROPRIORITY DTP IOSS-EXTRCOMP2  | ✅                      | GLS             |
  |      ER3     | EUROPRIORITY DTP IOSS-EXTRACOMP3 | ✅                      | GLS             |
  |      GXR     | GLOBALEXPRESS                    | ✅                      | FedEx           |
  |      GX1     | GLOBALEXPRESS-EXTRACOMP1         | ✅                      | FedEx           |
  |      GX2     | GLOBALEXPRESS-EXTRACOMP2         | ✅                      | FedEx           |
  |      GX3     | GLOBALEXPRESS-EXTRACOMP3         | ✅                      | FedEx           |
  |      ECA     | GLOBALPRIORITY EUROPE            | ⛔                      | N/A             |
  |      EC1     | GLOBALPRIORITY EUROPE-EXTRACOMP1 | ⛔                      | N/A             |
  |      EC2     | GLOBALPRIORITY EUROPE-EXTRACOMP2 | ⛔                      | N/A             |
  |      EC3     | GLOBALPRIORITY EUROPE-EXTRACOMP3 | ⛔                      | N/A             |
  |      GPA     | GLOBALPRIORITY ROW               | ⛔                      | N/A             |
  |      GP1     | GLOBALPRIORITY ROW-EXTRACOMP1    | ⛔                      | N/A             |
  |      GP2     | GLOBALPRIORITY ROW-EXTRACOMP2    | ⛔                      | N/A             |
  |      GP3     | GLOBALPRIORITY ROW-EXTRACOMP3    | ⛔                      | N/A             |
  |      IXA     | IRELAND EXPRESS                  | ✅                      | GLS             |
  |      IX1     | IRELAND EXPRESS-EXTRACOMP1       | ✅                      | GLS             |
  |      IX2     | IRELAND EXPRESS-EXTRACOMP2       | ✅                      | GLS             |
  |      IX3     | IRELAND EXPRESS-EXTRACOMP3       | ✅                      | GLS             |
  |      CEO     | China Economy - Personal Effects | ⛔                      | N/A             |
  |      CEP     | China Economy - POL Drop         | ⛔                      | N/A             |
  |      CEQ     | China Economy - Depot Drop       | ⛔                      | N/A             |
  |      CER     | China Economy - 3PC              | ⛔                      | N/A             |
  |      CES     | China Economy - Direct Hub Drop  | ⛔                      | N/A             |
</Accordion>