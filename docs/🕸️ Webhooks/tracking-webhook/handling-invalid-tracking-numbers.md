---
title: Register tracking numbers via Trackings API
excerpt: >-
  The _Trackings API_ provides a scalable, webhook‑driven approach to Royal Mail
  shipment tracking. By registering tracking numbers explicitly, customers gain
  proactive shipment visibility while maintaining control over tracking
  duration, volume, and costs.
deprecated: false
hidden: false
icon: fad fa-calendar-circle-exclamation
metadata:
  robots: index
---
Register Royal Mail tracking numbers with the [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API to receive webhook updates for eligible shipments created outside your standard INTERSOFT tracking flow.

<Callout icon="🛑" theme="error">
  ### _This endpoint is only supported for Royal Mail shipments and is a chargeable API feature. Customers should ensure tracking registration is performed only when required to avoid unnecessary costs._
</Callout>

INTERSOFT monitors each registered tracking number and pushes new events to your configured webhook for a defined tracking period.

Use this endpoint when you need:

- Automated shipment visibility
- Event‑driven tracking updates
- Integration‑based tracking without polling APIs

<Cards columns="3">
  <Card title="Royal Mail only" icon="fa-truck">
    This endpoint supports Royal Mail shipments only.
  </Card>

  <Card title="30-day tracking window" icon="fa-calendar">
    Tracking updates are retained and pushed for up to 30 days from registration.
  </Card>

  <Card title="Batch Processing" icon="fa-boxes-stacked">
    Submit up to 1,000 tracking numbers in a single `POST /v4/trackings` request.
  </Card>
</Cards>

# How it works

1. Create a Royal Mail shipment, or obtain valid Royal Mail tracking numbers.
2. Register the tracking numbers by submitting them to `POST /v4/trackings`.
3. INTERSOFT begins monitoring the registered shipments.
4. INTERSOFT pushes tracking updates to your webhook endpoint as events occur.

## Tracking window and delivery behaviour

- Tracking updates are retained and pushed for up to 30 days from registration.
- After the 30‑day tracking window expires, updates for the registered tracking numbers are no longer generated.
- Real-time tracking updates are delivered through webhook notifications.
- No historical tracking events are sent when a tracking number is registered. INTERSOFT pushes only events that occur after registration.

## Retry behaviour

If your webhook endpoint is temporarily unavailable, INTERSOFT retries delivery for up to 72 hours. After the retry window expires, undelivered events are discarded.

## Supported Royal Mail products

Tracking registration is supported only for the following Royal Mail trackable services:

<Accordion title="Domestic services" icon="fa-info-circle">
  | Product Code | Product Name                                         |
  | ------------ | ---------------------------------------------------- |
  | DE5          | Import UK Tracked 24 Parcel (TPM)(WH)                |
  | DE7          | Import UK Tracked 24 Parcel High Volume (AGE)(WH)    |
  | DE8          | Import UK Tracked 48 Parcel High Volume (AGE)(WH)    |
  | DE9          | Import UK Tracked 48 Parcel High Volume (AGE)        |
  | DEU          | Import UK Tracked 24 Parcel Boxable High Volume (WH) |
  | DEV          | Import UK Tracked 48 Parcel Boxable High Volume (WH) |
  | DEZ          | Import UK Tracked 48 Parcel (TPL)(WH)                |
  | FE0          | express48                                            |
  | FE1          | express48 Comp 1                                     |
  | FE2          | express48 Comp 2                                     |
  | FE3          | express48 Comp 3                                     |
  | FEA          | express48 Age                                        |
  | FEB          | express48 Age Comp 1                                 |
  | FEC          | express48 Age Comp 2                                 |
  | FED          | express48 Age Comp 3                                 |
  | FEE          | expressAM                                            |
  | FEF          | expressAM Comp 1                                     |
  | FEG          | expressAM Comp 2                                     |
  | FEK          | express24 Weekend                                    |
  | FEL          | expressAM Comp 3                                     |
  | FEM          | express48 Large                                      |
  | FEN          | express48 Large Comp 1                               |
  | FEO          | express48 Large Comp 2                               |
  | FEP          | express48 Large Comp 3                               |
  | FEQ          | express24 Weekend Comp 1                             |
  | FER          | express24 Weekend Comp 2                             |
  | FES          | express10 Comp 2                                     |
  | FET          | express10 Comp 3                                     |
  | FEU          | express24 Weekend Comp 3                             |
  | FEW          | expressAM Comp 1                                     |
  | FEX          | expressAM Comp 2                                     |
  | ITA          | Import Tracked Returns 24                            |
  | ITB          | Import Tracked Returns 48                            |
  | ITC          | Import Tracked 24 Boxable High Volume                |
  | ITD          | Import Tracked 48 Boxable High Volume                |
  | ITJ          | Import Tracked & Signed 24 High Volume (AGE)         |
  | ITL          | Import Tracked 48 High Volume                        |
  | ITM          | Import Tracked 24 High Volume                        |
  | M01          | Tracked 24 High Volume (PIN)                         |
  | M02          | Tracked 48 High Volume (PIN)                         |
  | M04          | Tracked 24 (PIN)                                     |
  | M05          | Tracked 48 (PIN)                                     |
  | M06          | Import Tracked 24 (PIN)                              |
  | M07          | expressAM Weekend Age                                |
  | M08          | expressAM Weekend Age Comp 1                         |
  | M09          | expressAM Weekend Age Comp 2                         |
  | M10          | expressAM Weekend Age Comp 3                         |
  | M13          | Import Tracked 48 (PIN)                              |
  | MA1          | expressAM Age                                        |
  | MA2          | expressAM Age Comp 1                                 |
  | MA3          | expressAM Age Comp 2                                 |
  | MA4          | expressAM Age Comp 3                                 |
  | MA6          | express48                                            |
  | ND0          | express10 Comp 1                                     |
  | NDA          | express24                                            |
  | NDB          | express24 Comp 1                                     |
  | NDC          | express24 Comp 2                                     |
  | NDE          | express24 Comp 3                                     |
  | NDF          | express24                                            |
  | NDG          | express24 Comp 1                                     |
  | NDH          | express24 Age                                        |
  | NDI          | express24 Age Comp 1                                 |
  | NDJ          | express24 Age Comp 2                                 |
  | NDK          | express24 Age Comp 3                                 |
  | NDM          | express24 Comp 2                                     |
  | NDN          | express24 Comp 3                                     |
  | NDO          | express24 Weekend Age                                |
  | NDP          | express48 Comp 1                                     |
  | NDQ          | express48 Comp 2                                     |
  | NDR          | express48 Comp 3                                     |
  | NDS          | express24 Weekend Age Comp 1                         |
  | NDT          | express24 Weekend Age Comp 2                         |
  | NDU          | expressAM Comp 3                                     |
  | NDV          | express24 Weekend Age Comp 3                         |
  | NDW          | express48 Large Comp 1                               |
  | NDX          | express48 Large Comp 2                               |
  | NDY          | express48 Large Comp 3                               |
  | PF0          | exams24                                              |
  | PF2          | expressAMF Comp 1                                    |
  | PF4          | expressAMF Comp 2                                    |
  | PF5          | expressAMF Comp 3                                    |
  | PF6          | expressAMF Weekend                                   |
  | PF7          | expressAMF Weekend Comp 1                            |
  | PF8          | expressAMF Weekend Comp 2                            |
  | PF9          | expressAMF Weekend Comp 3                            |
  | PFA          | exams10                                              |
  | PFB          | examsAM                                              |
  | PFD          | exams48                                              |
  | PFF          | examsAM Weekend                                      |
  | PFG          | exams24 Weekend                                      |
  | PFN          | exams24 Redelivery                                   |
  | PFQ          | expressAMF                                           |
  | RT0          | express24 Returns                                    |
  | RT1          | express24 Returns Comp 1                             |
  | RT2          | express24 Returns Comp 2                             |
  | RT3          | express24 Returns Comp 3                             |
  | RT4          | express24 with PIN Weekend                           |
  | RT5          | express24 with PIN Weekend Comp 1                    |
  | RTA          | express48 Returns                                    |
  | RTB          | express48 Returns Comp 1                             |
  | RTC          | express48 Returns Comp 2                             |
  | RTD          | express48 Returns Comp 3                             |
  | RTE          | express24 with PIN Weekend Comp 2                    |
  | RTF          | express24 with PIN Weekend Comp 3                    |
  | SD1          | Special Delivery Guaranteed by 1pm - £750            |
  | SD2          | Special Delivery Guaranteed by 1pm - £1000           |
  | SD3          | Special Delivery Guaranteed by 1pm - £2500           |
  | SD4          | Special Delivery Guaranteed by 9am - £750            |
  | SD5          | Special Delivery Guaranteed by 9am - £1000           |
  | SD6          | Special Delivery Guaranteed by 9am - £2500           |
  | SDA          | Special Delivery Guaranteed by 1pm (ID) - £750       |
  | SDB          | Special Delivery Guaranteed by 1pm (ID) - £1000      |
  | SDC          | Special Delivery Guaranteed by 1pm (ID) - £2500      |
  | SDE          | Special Delivery Guaranteed by 9am (ID) - £750       |
  | SDF          | Special Delivery Guaranteed by 9am (ID) - £1000      |
  | SDG          | Special Delivery Guaranteed by 9am (ID) - £2500      |
  | SDH          | Special Delivery Guaranteed by 1pm (AGE) - £750      |
  | SDJ          | Special Delivery Guaranteed by 1pm (AGE) - £1000     |
  | SDK          | Special Delivery Guaranteed by 1pm (AGE) - £2500     |
  | SDM          | Special Delivery Guaranteed by 9am (AGE) - £750      |
  | SDN          | Special Delivery Guaranteed by 9am (AGE) - £1000     |
  | SDQ          | Special Delivery Guaranteed by 9am (AGE) - £2500     |
  | SDV          | Special Delivery Guaranteed (AGE) - £750             |
  | SDW          | Special Delivery Guaranteed (AGE) - £1000            |
  | SDX          | Special Delivery Guaranteed (AGE) - £2500            |
  | SDY          | Special Delivery Guaranteed (ID) - £750              |
  | SDZ          | Special Delivery Guaranteed (ID) - £1000             |
  | SEA          | Special Delivery Guaranteed (ID) - £2500             |
  | SEB          | Special Delivery Guaranteed - £750                   |
  | SEC          | Special Delivery Guaranteed - £1000                  |
  | SED          | Special Delivery Guaranteed - £2500                  |
  | TA1          | express10 Age                                        |
  | TA2          | express10 Age Comp 1                                 |
  | TA3          | express10 Age Comp 2                                 |
  | TA4          | express10 Age Comp 3                                 |
  | TE1          | express10                                            |
  | TE2          | express10 Comp 1                                     |
  | TE3          | express10 Comp 2                                     |
  | TE4          | express10 Comp 3                                     |
  | TE5          | GLS ISRS                                             |
  | TEA          | express24 with PIN                                   |
  | TEB          | express24 with PIN Comp 1                            |
  | TEC          | express24 with PIN Comp 2                            |
  | TED          | express24 with PIN Comp 3                            |
  | TEF          | express10                                            |
  | TEG          | expressAM                                            |
  | TEH          | expressAM Weekend                                    |
  | TEI          | expressAM Weekend Comp 1                             |
  | TEJ          | expressAM Weekend Comp 2                             |
  | TEK          | expressAM Weekend Comp 3                             |
  | TEN          | express48 Large                                      |
  | TPA          | Tracked 24 High Volume (AGE) Signature               |
  | TPB          | Tracked 48 High Volume (AGE) Signature               |
  | TPC          | Tracked 24 (AGE) Signature                           |
  | TPD          | Tracked 48 (AGE) Signature                           |
  | TPL          | Tracked 48 High Volume (Optional Signature)          |
  | TPM          | Tracked 24 High Volume (Optional Signature)          |
  | TPN          | Tracked 24 (Optional Signature)                      |
  | TPS          | Tracked 48 (Optional Signature)                      |
  | TRL          | Tracked 48 Boxable High Volume (Optional Signature)  |
  | TRM          | Tracked 24 Boxable High Volume (Optional Signature)  |
  | TRN          | Tracked 24 Boxable (Optional Signature)              |
  | TRS          | Tracked 48 Boxable (Optional Signature)              |
  | TSN          | Tracked Returns 24                                   |
  | TSS          | Tracked Returns 48                                   |
</Accordion>

<Accordion title="International services" icon="fa-info-circle">
  | Product Code | Product Name                                                                       |
  | ------------ | ---------------------------------------------------------------------------------- |
  | BU3          | INTL IMP TRK PCL XCOMP CTRY PDDP                                                   |
  | BU5          | INTL IMP TRK PCL DDP                                                               |
  | BXC          | International Business Parcels Tracked Country Priced Boxable Extra Comp           |
  | BXE          | International Business Parcels Tracked Country Priced Boxable DDP                  |
  | BXF          | International Business Parcels Tracked Country Priced Boxable                      |
  | BZU          | Intl Bus Parcels Tracked Extra Comp Ctry PDDP                                      |
  | BZX          | Intl Business-NPC-TRK-LLTR PDDP                                                    |
  | DE0          | Cross Border Parcels Tracked 0-30kg (EMS)                                          |
  | DEI          | Cross Border Parcels Tracked                                                       |
  | ETA          | International Parcels Tracked ETOE                                                 |
  | ETD          | International Large Letters Tracked ETOE                                           |
  | ETG          | International Parcels Tracked 0-30kg ETOE (E)                                      |
  | ETH          | International Parcels Tracked 0-30kg Extra Comp ETOE (E)                           |
  | ETL          | International Business PC Letters Tracked ETOE                                     |
  | ETP          | International Business PC Large Letters Tracked ETOE                               |
  | HVB          | International Parcels Tracked 0-30kg                                               |
  | HVE          | International Parcels Tracked 0-30kg Extra Comp                                    |
  | IT2          | International Business Parcels Tracked (Repair-VAT Exc)                            |
  | IT3          | International Business Parcels Tracked (Repair-VAT Pay)                            |
  | IT4          | International Business Parcels Tracked (Network)                                   |
  | IT5          | International Business Large Letters Tracked (Network)                             |
  | IT6          | International Business Parcels Tracked Country Priced Boxable (Network)            |
  | ITO          | Cross Border Parcels Tracked Extra Comp 0-30kg (EMS)                               |
  | ITQ          | Cross Border Parcels Tracked 0-30kg (INCNCT)                                       |
  | ITT          | Cross Border Parcels Tracked Extra Comp 0-30kg (INCNCT)                            |
  | LLH          | International Business NPC Large Letters Tracked Zone Sort                         |
  | LLK          | International Business NPC Large Letters Tracked Zone Sort Extra Comp              |
  | LLN          | International Business NPC Large Letters Tracked Country Priced Extra Comp         |
  | MP1          | International Business Parcels Tracked Zone Sort                                   |
  | MP4          | International Business Parcels Tracked Extra Comp Zone Sort                        |
  | MP7          | International Business Parcels Tracked Country Priced                              |
  | MP8          | International Business Parcels Tracked Extra Comp Country Priced                   |
  | MPR          | International Business Parcel Tracked Country Priced                               |
  | MQ1          | Int Bus Trck Prcls Flat Rate                                                       |
  | MQ2          | Int Bus Trck Prcls Flt Rt Xcmp                                                     |
  | MTK          | International Business Mail Tracked Country Priced                                 |
  | MTS          | International Business Parcels Tracked Direct Ireland Country                      |
  | OTA          | International Tracked On Account                                                   |
  | OTB          | International Tracked On Account Extra Comp                                        |
  | TIA          | International Business Parcels Tracked 0-30kg Extra Comp (R)                       |
  | TIB          | International Business Parcels Tracked 0-30kg Extra Comp (C)                       |
  | TIE          | International Business Parcels Semi-Tracked                                        |
  | TIF          | International Business Large Letters Semi-Tracked                                  |
  | TIH          | International Business Parcels Tracked Express (LQ)                                |
  | BU1          | INTL IMP TRK PCL 0-30kg C PDDP                                                     |
  | BU2          | INTL IMP TRK PCL 0-30kg C XCOMP PDDP                                               |
  | BYB          | International Tracked Parcels DDP                                                  |
  | BYD          | International Business Tracked Heavier DDP                                         |
  | BYH          | International Business Tracked Heavier DDP Extra Comp                              |
  | BYL          | INT BUS PCL TRK HVR IOSS DDP Comp 2                                                |
  | BYM          | INT BUS PCL TRK HVR IOSS DDP Comp 3                                                |
  | ETI          | International Parcels Tracked 0-30kg ETOE (C)                                      |
  | ETJ          | International Parcels Tracked 0-30kg Extra Comp ETOE (C)                           |
  | HVD          | International Business NPC Tracked Priority                                        |
  | HVK          | International Parcels Tracked 0-30kg C Priority                                    |
  | HVL          | International Parcels Tracked 0-30kg Extra Comp C Priority                         |
  | ISD          | International Business Tracked Priority Extra Comp                                 |
  | RC1          | INTL Trk Parcels 0-30kg E PDDP                                                     |
  | RC2          | INTL Trk Parcels 0-30kg E PDDP Comp 1                                              |
  | RC3          | INTL Trk Parcels 0-30kg E PDDP Comp 2                                              |
  | RC4          | INTL Trk Parcels 0-30kg E PDDP Comp 3                                              |
  | BZV          | INTL BUS PARCEL TRACK\&SIGN XTR CMP CTRY PDDP                                      |
  | BZY          | INTL BUSINESS-NPC-TRKSGN-LLTR PDDP                                                 |
  | ETB          | International Parcels Tracked & Signed ETOE                                        |
  | ETE          | International Large Letters Tracked & Signed ETOE                                  |
  | ETM          | International Business PC Letters Tracked & Signed ETOE                            |
  | ETQ          | International Business PC Large Letters Tracked & Signed ETOE                      |
  | ITW          | Cross Border Parcels Tracked & Signed Extra Comp 0-30kg (EMS)                      |
  | ITY          | Cross Border Parcels Tracked & Signed Extra Comp 0-30kg (INCNCT)                   |
  | IYX          | Cross Border Parcels Tracked & Signed 0-30kg (INCNCT)                              |
  | MPM          | International Business Mail Tracked & Signed High Volume Country Priced            |
  | MPP          | International Business Mail Tracked & Signed High Volume Extra Comp Country Priced |
  | MTC          | International Business Mail Tracked & Signed Zone Sort                             |
  | OTC          | International Tracked & Signed On Account                                          |
  | OTD          | International Tracked & Signed On Account Extra Comp                               |
  | CEO          | China Economy - Personal Effects                                                   |
  | CEP          | China Economy - POL Drop                                                           |
  | CEQ          | China Economy - Depot Drop                                                         |
  | CER          | China Economy - 3PC                                                                |
  | CES          | China Economy - Direct Hub Drop                                                    |
  | EC1          | globalpriority Europe Comp 1                                                       |
  | EC2          | globalpriority Europe Comp 2                                                       |
  | EC3          | globalpriority Europe Comp 3                                                       |
  | ECA          | globalpriority Europe                                                              |
  | ER1          | europriority DTP IOSS Comp 1                                                       |
  | ER2          | europriority DTP IOSS Comp 2                                                       |
  | ER3          | europriority DTP IOSS Comp 3                                                       |
  | ER6          | europriority DDP Comp 1                                                            |
  | ER7          | europriority DDP Comp 2                                                            |
  | ER8          | europriority DDP Comp 3                                                            |
  | ERA          | europriority DTP IOSS                                                              |
  | ERB          | europriority DDP                                                                   |
  | GE1          | globalexpress DDP                                                                  |
  | GE2          | globalexpress DDP Comp 1                                                           |
  | GE3          | globalexpress DDP Comp 2                                                           |
  | GE4          | globalexpress DDP Comp 3                                                           |
  | GP1          | globalpriority ROW Comp 1                                                          |
  | GP2          | globalpriority ROW Comp 2                                                          |
  | GP3          | globalpriority ROW Comp 3                                                          |
  | GPA          | globalpriority ROW                                                                 |
  | GX1          | globalexpress Comp 1                                                               |
  | GX2          | globalexpress Comp 2                                                               |
  | GX3          | globalexpress Comp 3                                                               |
  | GXR          | globalexpress                                                                      |
  | IX1          | irelandexpress Comp 1                                                              |
  | IX2          | irelandexpress Comp 2                                                              |
  | IX3          | irelandexpress Comp 3                                                              |
  | IXA          | irelandexpress                                                                     |
  | EC4          | globalpriority ROW                                                                 |
  | EC5          | globalpriority ROW Comp 1                                                          |
  | EC6          | globalpriority ROW Comp 2                                                          |
  | EC7          | globalpriority ROW Comp 3                                                          |
  | ER0          | globalexpress Comp 3                                                               |
  | ER4          | globalexpress                                                                      |
  | ER5          | globalexpress Comp 1                                                               |
  | ER9          | globalexpress Comp 2                                                               |
  | GP4          | globalpriority Europe                                                              |
  | GP5          | globalpriority Europe Comp 1                                                       |
  | GP6          | globalpriority Europe Comp 2                                                       |
  | GP7          | globalpriority Europe Comp 3                                                       |
  | GX4          | irelandexpress Comp 2                                                              |
  | GX5          | irelandexpress Comp 3                                                              |
  | IX4          | irelandexpress                                                                     |
  | IX5          | irelandexpress Comp 1                                                              |
</Accordion>

<Callout icon="far fa-circle-info" theme="info">
  ### _Note_

  _Tracking registration requests submitted for unsupported services will not return tracking updates._
</Callout>

# Handle invalid tracking numbers

If a batch contains invalid tracking numbers, the [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API continues processing the valid ones and reports the invalid entries separately.

<Cards columns="2">
  <Card title="Processing behaviour" icon="fa-cogs">
    - All tracking numbers in a request are accepted and inserted into the database, up to 1,000 entries per request.
    - Invalid tracking numbers are marked as `DO NOT TRACK` and are not registered with the carrier.
    - The request does not fail when invalid numbers are present.
    - Duplicate tracking numbers within the same batch are accepted.
  </Card>

  <Card title="Invalid tracking event" icon="fa-exclamation-triangle">
    For each invalid tracking number, Intersoft creates a tracking event and pushes it to your webhook.

    **Event properties**

    - **Event code:** `INVD`
    - **Event name:** `Invalid Tracking Number`
    - **Event type:** `Tracking`
    - **Milestone:** `No`
    - **Stop the clock:** `Yes`
  </Card>
</Cards>

<Callout icon="📘" theme="info">
  ### _Note_

  _The webhook payload includes the mandatory fields shown in the&#x20;_[push payload example](https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample)_. Invalid tracking numbers are processed asynchronously so valid shipments continue tracking without interruption._
</Callout>

***

### See also

<Cards columns="3">
  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus" target="_blank">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up" target="_blank">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>
