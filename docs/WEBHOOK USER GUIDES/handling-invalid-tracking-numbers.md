---
title: Handling invalid tracking numbers
deprecated: false
hidden: true
icon: fad fa-warehouse
metadata:
  robots: index
---
<br />

Background
The Sapient /trackings API allows customers (so called data processors) to submit/ register a tracking number with Intersoft. It is used to provide tracking information back to the customer for shipments where they did not create the shipping label and only need the tracking information.
The existing functionality allows customers to register up to 1000 tracking numbers in a single request. However, handling the request failure is not very usable. If one tracking number in the request is invalid, the system will error the whole request and return an unhelpful error response. Due to this behaviour customer tend to supply one tracking number per request, but facing throttling issues when trying to register a high volume of shipments.
To address these limitations, the API logic must be enhanced to process valid tracking numbers within a batch while isolating invalid entries. Invalid tracking numbers should not prevent successful processing of the remaining batch. Additionally, the system must provide clear, actionable feedback for invalid entries, enabling customers to identify and correct errors without impacting overall submission efficiency.

Solution and handling
•	System to accept all tracking numbers supplied in a single API request and insert them into the database (Max of 1000 – existing process)
•	System to identify invalid tracking numbers and mark them as ‘DO NOT TRACK’ and do not register them with Royal Mail.
•	For each of the invalid tracking number identified, a tracking event must be created and pushed to the customer via the tracking webhook
•	The invalid tracking number event must be populated as below;
o   Event code: INVD
o   Event name: Invalid Tracking Number
o   Event type: Tracking
o   Not to be added as a milestone
o   Event to be a stop the clock event
•	The expected tracking webhook payload for an invalid tracking number to be as per below JSON file with the mandatory fields highlighted in yellow
•	The request will not fail if invalid tracking numbers are supplied; only invalid numbers will be marked accordingly.
•	Duplicate tracking number within same API batch will not be rejected
