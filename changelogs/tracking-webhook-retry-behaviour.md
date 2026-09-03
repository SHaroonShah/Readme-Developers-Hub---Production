---
title: Tracking Webhook retry logic updates
author: Syed Haroon Shah
hidden: true
published_at: '2026-05-12T15:12:56.986Z'
type: improved
---
INTERSOFT Tracking Webhook delivery continues to follow the existing retry policy. Previously, certain errors caused the webhook to be suspended immediately, resulting in failed delivery attempts. This behaviour has been updated so that all delivery errors now enter the retry process rather than triggering immediate suspension. Once the retry limit is exhausted and the webhook becomes suspended, it remains suspended and no further delivery attempts or retries are performed.

<br />