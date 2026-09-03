---
title: Error Classification and Retry Mechanism Updated in Tracking Webhook
author: Millie Deiry
hidden: true
published_at: '2024-08-07T13:09:41.125Z'
type: improved
---
The Tracking Webhook system has been updated to classify all HTTP responses from the carrier API outside the HTTP 200-299 range as errors and return the corresponding error response. Additionally, the retry mechanism has been revised to cease retry attempts to fetch tracking data from the carrier API after 24 hours of continuous failure, following specific retry intervals.