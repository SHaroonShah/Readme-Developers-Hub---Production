---
title: Royal Mail Integration Update to Allow Limited Quantity Dangerous Goods (LQDG)
author: Millie Deiry
hidden: true
published_at: '2024-03-11T15:04:27.092Z'
type: added
---
The Royal Mail integration has been updated to allow shipments to be created containing Limited Quantity Dangerous Goods. LQDG is currently available with Tracked 48 services only and for shipments with a maximum weight of 10kg or less. The Add Product endpoint and Royal Mail Create Shipment endpoint have both been updated to include a Hazmat endpoint which can be used for providing LQDG information, and Hazmat fields have also been added to the Product UI. When a Royal Mail shipment is created with either hazmat information provided in the Create Shipment request or using a stored product with hazmat information provided for the product, it will be validated as an LQDG shipment. Providing the shipment is using a valid service, has a total weight of 10kg or less, and the hazardous UN Class and destination postcode are supported by Royal Mail for LQDG shipments, then the shipment will be successfully created as an LQDG shipment and the label will contain a “Do not fly” statement.

LQDG can also be used with offline barcodes and pre-allocated tracking numbers.

> 📘 See the API Reference page for more information on the updates to the Add Product and Royal Mail Create Shipment endpoints.