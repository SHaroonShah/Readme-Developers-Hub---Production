---
title: Handling invalid tracking numbers
deprecated: false
hidden: true
icon: fad fa-calendar-circle-exclamation
metadata:
  robots: index
---
## Overview

The Sapient;'s [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) processes valid tracking numbers while isolating the invalid ones, providing clear feedback without failing the entire batch.

## Handling procedure

<Cards columns={2}>
  <Card title="Processing Behavior" icon="fa-cogs">
    * All tracking numbers in a request are accepted and inserted into the database (max 1000)
    * Invalid tracking numbers are marked as 'DO NOT TRACK' and not registered with the carrier
    * Requests does not fail if invalid numbers are present—only invalid entries are marked accordingly
    * Duplicate tracking numbers within the same batch are accepted
  </Card>

  <Card title="Invalid Tracking Events" icon="fa-exclamation-triangle">
    For each invalid tracking number, a tracking event is created and pushed via webhook.

    **Event Properties:**

    * **Event code:** `INVD`
    * **Event name:** Invalid Tracking Number
    * **Event type:** Tracking
    * **Milestone:** No
    * **Stop the clock:** Yes
  </Card>
</Cards>

<Accordion title="Technical Details" icon="fa-info-circle">
  The webhook payload includes mandatory fields as specified in the reference JSON file. Invalid tracking numbers are processed asynchronously to ensure valid shipments continue tracking without interruption.
</Accordion>
