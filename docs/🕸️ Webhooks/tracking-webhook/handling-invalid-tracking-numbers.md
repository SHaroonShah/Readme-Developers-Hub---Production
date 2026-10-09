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

## Supported Royal Mail services

Tracking registration is supported only for the following Royal Mail trackable services:

<Accordion title="Domestic services">
  | Service Code | Service Name                                         |
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

<Accordion title="International services">
  <Table>
    <thead>
      <tr>
        <th style={{ width: "20.9%" }}>
          Service Code
        </th>

        <th style={{ width: "79%" }}>
          Service Name
        </th>
      </tr>
    </thead>

    <tbody>
      <tr>
        <td>
          BU3
        </td>

        <td>
          INTL IMP TRK PCL XCOMP CTRY PDDP
        </td>
      </tr>

      <tr>
        <td>
          BU5
        </td>

        <td>
          INTL IMP TRK PCL DDP
        </td>
      </tr>

      <tr>
        <td>
          BXC
        </td>

        <td>
          International Business Parcels Tracked Country Priced Boxable Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          BXE
        </td>

        <td>
          International Business Parcels Tracked Country Priced Boxable DDP
        </td>
      </tr>

      <tr>
        <td>
          BXF
        </td>

        <td>
          International Business Parcels Tracked Country Priced Boxable
        </td>
      </tr>

      <tr>
        <td>
          BZU
        </td>

        <td>
          Intl Bus Parcels Tracked Extra Comp Ctry PDDP
        </td>
      </tr>

      <tr>
        <td>
          BZX
        </td>

        <td>
          Intl Business-NPC-TRK-LLTR PDDP
        </td>
      </tr>

      <tr>
        <td>
          DE0
        </td>

        <td>
          Cross Border Parcels Tracked 0-30kg (EMS)
        </td>
      </tr>

      <tr>
        <td>
          DEI
        </td>

        <td>
          Cross Border Parcels Tracked
        </td>
      </tr>

      <tr>
        <td>
          ETA
        </td>

        <td>
          International Parcels Tracked ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETD
        </td>

        <td>
          International Large Letters Tracked ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETG
        </td>

        <td>
          International Parcels Tracked 0-30kg ETOE (E)
        </td>
      </tr>

      <tr>
        <td>
          ETH
        </td>

        <td>
          International Parcels Tracked 0-30kg Extra Comp ETOE (E)
        </td>
      </tr>

      <tr>
        <td>
          ETL
        </td>

        <td>
          International Business PC Letters Tracked ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETP
        </td>

        <td>
          International Business PC Large Letters Tracked ETOE
        </td>
      </tr>

      <tr>
        <td>
          HVB
        </td>

        <td>
          International Parcels Tracked 0-30kg
        </td>
      </tr>

      <tr>
        <td>
          HVE
        </td>

        <td>
          International Parcels Tracked 0-30kg Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          IT2
        </td>

        <td>
          International Business Parcels Tracked (Repair-VAT Exc)
        </td>
      </tr>

      <tr>
        <td>
          IT3
        </td>

        <td>
          International Business Parcels Tracked (Repair-VAT Pay)
        </td>
      </tr>

      <tr>
        <td>
          IT4
        </td>

        <td>
          International Business Parcels Tracked (Network)
        </td>
      </tr>

      <tr>
        <td>
          IT5
        </td>

        <td>
          International Business Large Letters Tracked (Network)
        </td>
      </tr>

      <tr>
        <td>
          IT6
        </td>

        <td>
          International Business Parcels Tracked Country Priced Boxable (Network)
        </td>
      </tr>

      <tr>
        <td>
          ITO
        </td>

        <td>
          Cross Border Parcels Tracked Extra Comp 0-30kg (EMS)
        </td>
      </tr>

      <tr>
        <td>
          ITQ
        </td>

        <td>
          Cross Border Parcels Tracked 0-30kg (INCNCT)
        </td>
      </tr>

      <tr>
        <td>
          ITT
        </td>

        <td>
          Cross Border Parcels Tracked Extra Comp 0-30kg (INCNCT)
        </td>
      </tr>

      <tr>
        <td>
          LLH
        </td>

        <td>
          International Business NPC Large Letters Tracked Zone Sort
        </td>
      </tr>

      <tr>
        <td>
          LLK
        </td>

        <td>
          International Business NPC Large Letters Tracked Zone Sort Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          LLN
        </td>

        <td>
          International Business NPC Large Letters Tracked Country Priced Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          MP1
        </td>

        <td>
          International Business Parcels Tracked Zone Sort
        </td>
      </tr>

      <tr>
        <td>
          MP4
        </td>

        <td>
          International Business Parcels Tracked Extra Comp Zone Sort
        </td>
      </tr>

      <tr>
        <td>
          MP7
        </td>

        <td>
          International Business Parcels Tracked Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MP8
        </td>

        <td>
          International Business Parcels Tracked Extra Comp Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MPR
        </td>

        <td>
          International Business Parcel Tracked Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MQ1
        </td>

        <td>
          Int Bus Trck Prcls Flat Rate
        </td>
      </tr>

      <tr>
        <td>
          MQ2
        </td>

        <td>
          Int Bus Trck Prcls Flt Rt Xcmp
        </td>
      </tr>

      <tr>
        <td>
          MTK
        </td>

        <td>
          International Business Mail Tracked Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MTS
        </td>

        <td>
          International Business Parcels Tracked Direct Ireland Country
        </td>
      </tr>

      <tr>
        <td>
          OTA
        </td>

        <td>
          International Tracked On Account
        </td>
      </tr>

      <tr>
        <td>
          OTB
        </td>

        <td>
          International Tracked On Account Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          TIA
        </td>

        <td>
          International Business Parcels Tracked 0-30kg Extra Comp (R)
        </td>
      </tr>

      <tr>
        <td>
          TIB
        </td>

        <td>
          International Business Parcels Tracked 0-30kg Extra Comp (C)
        </td>
      </tr>

      <tr>
        <td>
          TIE
        </td>

        <td>
          International Business Parcels Semi-Tracked
        </td>
      </tr>

      <tr>
        <td>
          TIF
        </td>

        <td>
          International Business Large Letters Semi-Tracked
        </td>
      </tr>

      <tr>
        <td>
          TIH
        </td>

        <td>
          International Business Parcels Tracked Express (LQ)
        </td>
      </tr>

      <tr>
        <td>
          BU1
        </td>

        <td>
          INTL IMP TRK PCL 0-30kg C PDDP
        </td>
      </tr>

      <tr>
        <td>
          BU2
        </td>

        <td>
          INTL IMP TRK PCL 0-30kg C XCOMP PDDP
        </td>
      </tr>

      <tr>
        <td>
          BYB
        </td>

        <td>
          International Tracked Parcels DDP
        </td>
      </tr>

      <tr>
        <td>
          BYD
        </td>

        <td>
          International Business Tracked Heavier DDP
        </td>
      </tr>

      <tr>
        <td>
          BYH
        </td>

        <td>
          International Business Tracked Heavier DDP Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          BYL
        </td>

        <td>
          INT BUS PCL TRK HVR IOSS DDP Comp 2
        </td>
      </tr>

      <tr>
        <td>
          BYM
        </td>

        <td>
          INT BUS PCL TRK HVR IOSS DDP Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ETI
        </td>

        <td>
          International Parcels Tracked 0-30kg ETOE (C)
        </td>
      </tr>

      <tr>
        <td>
          ETJ
        </td>

        <td>
          International Parcels Tracked 0-30kg Extra Comp ETOE (C)
        </td>
      </tr>

      <tr>
        <td>
          HVD
        </td>

        <td>
          International Business NPC Tracked Priority
        </td>
      </tr>

      <tr>
        <td>
          HVK
        </td>

        <td>
          International Parcels Tracked 0-30kg C Priority
        </td>
      </tr>

      <tr>
        <td>
          HVL
        </td>

        <td>
          International Parcels Tracked 0-30kg Extra Comp C Priority
        </td>
      </tr>

      <tr>
        <td>
          ISD
        </td>

        <td>
          International Business Tracked Priority Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          RC1
        </td>

        <td>
          INTL Trk Parcels 0-30kg E PDDP
        </td>
      </tr>

      <tr>
        <td>
          RC2
        </td>

        <td>
          INTL Trk Parcels 0-30kg E PDDP Comp 1
        </td>
      </tr>

      <tr>
        <td>
          RC3
        </td>

        <td>
          INTL Trk Parcels 0-30kg E PDDP Comp 2
        </td>
      </tr>

      <tr>
        <td>
          RC4
        </td>

        <td>
          INTL Trk Parcels 0-30kg E PDDP Comp 3
        </td>
      </tr>

      <tr>
        <td>
          BZV
        </td>

        <td>
          INTL BUS PARCEL TRACK\&SIGN XTR CMP CTRY PDDP
        </td>
      </tr>

      <tr>
        <td>
          BZY
        </td>

        <td>
          INTL BUSINESS-NPC-TRKSGN-LLTR PDDP
        </td>
      </tr>

      <tr>
        <td>
          ETB
        </td>

        <td>
          International Parcels Tracked & Signed ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETE
        </td>

        <td>
          International Large Letters Tracked & Signed ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETM
        </td>

        <td>
          International Business PC Letters Tracked & Signed ETOE
        </td>
      </tr>

      <tr>
        <td>
          ETQ
        </td>

        <td>
          International Business PC Large Letters Tracked & Signed ETOE
        </td>
      </tr>

      <tr>
        <td>
          ITW
        </td>

        <td>
          Cross Border Parcels Tracked & Signed Extra Comp 0-30kg (EMS)
        </td>
      </tr>

      <tr>
        <td>
          ITY
        </td>

        <td>
          Cross Border Parcels Tracked & Signed Extra Comp 0-30kg (INCNCT)
        </td>
      </tr>

      <tr>
        <td>
          IYX
        </td>

        <td>
          Cross Border Parcels Tracked & Signed 0-30kg (INCNCT)
        </td>
      </tr>

      <tr>
        <td>
          MPM
        </td>

        <td>
          International Business Mail Tracked & Signed High Volume Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MPP
        </td>

        <td>
          International Business Mail Tracked & Signed High Volume Extra Comp Country Priced
        </td>
      </tr>

      <tr>
        <td>
          MTC
        </td>

        <td>
          International Business Mail Tracked & Signed Zone Sort
        </td>
      </tr>

      <tr>
        <td>
          OTC
        </td>

        <td>
          International Tracked & Signed On Account
        </td>
      </tr>

      <tr>
        <td>
          OTD
        </td>

        <td>
          International Tracked & Signed On Account Extra Comp
        </td>
      </tr>

      <tr>
        <td>
          CEO
        </td>

        <td>
          China Economy - Personal Effects
        </td>
      </tr>

      <tr>
        <td>
          CEP
        </td>

        <td>
          China Economy - POL Drop
        </td>
      </tr>

      <tr>
        <td>
          CEQ
        </td>

        <td>
          China Economy - Depot Drop
        </td>
      </tr>

      <tr>
        <td>
          CER
        </td>

        <td>
          China Economy - 3PC
        </td>
      </tr>

      <tr>
        <td>
          CES
        </td>

        <td>
          China Economy - Direct Hub Drop
        </td>
      </tr>

      <tr>
        <td>
          EC1
        </td>

        <td>
          globalpriority Europe Comp 1
        </td>
      </tr>

      <tr>
        <td>
          EC2
        </td>

        <td>
          globalpriority Europe Comp 2
        </td>
      </tr>

      <tr>
        <td>
          EC3
        </td>

        <td>
          globalpriority Europe Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ECA
        </td>

        <td>
          globalpriority Europe
        </td>
      </tr>

      <tr>
        <td>
          ER1
        </td>

        <td>
          europriority DTP IOSS Comp 1
        </td>
      </tr>

      <tr>
        <td>
          ER2
        </td>

        <td>
          europriority DTP IOSS Comp 2
        </td>
      </tr>

      <tr>
        <td>
          ER3
        </td>

        <td>
          europriority DTP IOSS Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ER6
        </td>

        <td>
          europriority DDP Comp 1
        </td>
      </tr>

      <tr>
        <td>
          ER7
        </td>

        <td>
          europriority DDP Comp 2
        </td>
      </tr>

      <tr>
        <td>
          ER8
        </td>

        <td>
          europriority DDP Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ERA
        </td>

        <td>
          europriority DTP IOSS
        </td>
      </tr>

      <tr>
        <td>
          ERB
        </td>

        <td>
          europriority DDP
        </td>
      </tr>

      <tr>
        <td>
          GE1
        </td>

        <td>
          globalexpress DDP
        </td>
      </tr>

      <tr>
        <td>
          GE2
        </td>

        <td>
          globalexpress DDP Comp 1
        </td>
      </tr>

      <tr>
        <td>
          GE3
        </td>

        <td>
          globalexpress DDP Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GE4
        </td>

        <td>
          globalexpress DDP Comp 3
        </td>
      </tr>

      <tr>
        <td>
          GP1
        </td>

        <td>
          globalpriority ROW Comp 1
        </td>
      </tr>

      <tr>
        <td>
          GP2
        </td>

        <td>
          globalpriority ROW Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GP3
        </td>

        <td>
          globalpriority ROW Comp 3
        </td>
      </tr>

      <tr>
        <td>
          GPA
        </td>

        <td>
          globalpriority ROW
        </td>
      </tr>

      <tr>
        <td>
          GX1
        </td>

        <td>
          globalexpress Comp 1
        </td>
      </tr>

      <tr>
        <td>
          GX2
        </td>

        <td>
          globalexpress Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GX3
        </td>

        <td>
          globalexpress Comp 3
        </td>
      </tr>

      <tr>
        <td>
          GXR
        </td>

        <td>
          globalexpress
        </td>
      </tr>

      <tr>
        <td>
          IX1
        </td>

        <td>
          irelandexpress Comp 1
        </td>
      </tr>

      <tr>
        <td>
          IX2
        </td>

        <td>
          irelandexpress Comp 2
        </td>
      </tr>

      <tr>
        <td>
          IX3
        </td>

        <td>
          irelandexpress Comp 3
        </td>
      </tr>

      <tr>
        <td>
          IXA
        </td>

        <td>
          irelandexpress
        </td>
      </tr>

      <tr>
        <td>
          EC4
        </td>

        <td>
          globalpriority ROW
        </td>
      </tr>

      <tr>
        <td>
          EC5
        </td>

        <td>
          globalpriority ROW Comp 1
        </td>
      </tr>

      <tr>
        <td>
          EC6
        </td>

        <td>
          globalpriority ROW Comp 2
        </td>
      </tr>

      <tr>
        <td>
          EC7
        </td>

        <td>
          globalpriority ROW Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ER0
        </td>

        <td>
          globalexpress Comp 3
        </td>
      </tr>

      <tr>
        <td>
          ER4
        </td>

        <td>
          globalexpress
        </td>
      </tr>

      <tr>
        <td>
          ER5
        </td>

        <td>
          globalexpress Comp 1
        </td>
      </tr>

      <tr>
        <td>
          ER9
        </td>

        <td>
          globalexpress Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GP4
        </td>

        <td>
          globalpriority Europe
        </td>
      </tr>

      <tr>
        <td>
          GP5
        </td>

        <td>
          globalpriority Europe Comp 1
        </td>
      </tr>

      <tr>
        <td>
          GP6
        </td>

        <td>
          globalpriority Europe Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GP7
        </td>

        <td>
          globalpriority Europe Comp 3
        </td>
      </tr>

      <tr>
        <td>
          GX4
        </td>

        <td>
          irelandexpress Comp 2
        </td>
      </tr>

      <tr>
        <td>
          GX5
        </td>

        <td>
          irelandexpress Comp 3
        </td>
      </tr>

      <tr>
        <td>
          IX4
        </td>

        <td>
          irelandexpress
        </td>
      </tr>

      <tr>
        <td>
          IX5
        </td>

        <td>
          irelandexpress Comp 1
        </td>
      </tr>
    </tbody>
  </Table>
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
