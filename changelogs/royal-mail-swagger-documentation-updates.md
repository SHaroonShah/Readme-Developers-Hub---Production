---
title: DPD UK swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2026-05-12T09:35:50.547Z'
type: improved
---
A new **CarrierDetails** > **Barcode** field has been added at the **Packages** level in the **Create Shipment** endpoint response, allowing users to scan and track shipments and match them against the stored barcode information.

```curl
"LabelFormat": "PDF",
    "Packages": [
        {
            "CarrierDetails": {
                "Barcode": "%BT370QB15501999000067812826"
            },
            "PackageOccurrence": 1,
            "TrackingNumber": "15501999000067",
            "CarrierTrackingUrl": "https://track.dpd.co.uk/search?reference=15501999000067"
        }
    ]

```

<p style={{ textAlign: "center" }}>
  <em>Response payload example</em>
</p>