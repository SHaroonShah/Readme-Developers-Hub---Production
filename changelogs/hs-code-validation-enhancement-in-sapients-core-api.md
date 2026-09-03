---
title: HS Code validation enhancement in SAPIENT's core API
author: Syed Haroon Shah
hidden: true
published_at: '2025-07-25T11:11:50.116Z'
type: improved
---
The **Hurricane Services** API endpoint of the Sapient Core API is now enhanced to support HS codes longer than 10 digits, enabling accurate code validation for countries like Qatar and Kuwait. The **Commodity Codes Validation** endpoint will send requests to Hurricane’s Quick Check API. In response, two new fields—**originalImportCode** and **originalExportCode**—will be included under the **Items** object, providing the correct codes directly from the Hurricane service. The originalImportCode and originalExportCode fields aren't currently being populated, but have been added to the Commodity Codes Validation response in preparation for future use.