---
title: Handle invalid tracking numbers
author: Syed Haroon Shah
hidden: true
published_at: '2026-04-01T14:31:10.491Z'
type: improved
---
The SAPIENT's **Trackings** API  has been enhanced to improve visibility and handling of invalid tracking numbers submitted in batch requests.

The API now accepts and processes all tracking numbers supplied in a single request (up to 1,000), without failing the entire batch when invalid entries are present. Valid tracking numbers are registered as normal, while invalid tracking numbers are identified and excluded from registration with Royal Mail.

Invalid tracking numbers are automatically marked as "DO NOT TRACK," and a corresponding tracking event is generated and sent to the customer via the Intersoft tracking webhook. This event provides clear feedback without impacting the processing of valid tracking numbers.

> 📘 _Note_
>
> _For more information, refer to the [Handle invalid tracking numbers](https://docs.intersoftsapient.net/docs/handling-invalid-tracking-numbers) guide._