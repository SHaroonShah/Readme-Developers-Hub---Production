---
title: Webhook suspension
excerpt: >-
  _Webhook suspension_ refers to the disabling of the webhook notifications for
  shipment events due to an error.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If the receiving endpoint (the system where the notifications are sent) is down or encounters errors, for example, time out, invalid data, SAPIENT may suspend sending further webhook notifications to avoid overwhelming the system. 

If the threshold value for retrying the webhook within the given intervals is exceeded, then the webhook is suspended and a corresponding email is sent to the primary user registered for the customer. A _primary user_ is set up at the time of customer onboarding. If you want to change the primary user, you can contact Intersoft's onboarding team.

> 💡 _Tip_
> 
> _The webhook can be [activated](https://docs.intersoftsapient.net/docs/create-tracking-webhook) via the GUI._

The retry intervals for the webhook are provided in the following table.

| ShipmentTrackingStatusRetryIntervalId | RetryCount | IntervalInMinutes |
| :-----------------------------------: | :--------- | :---------------- |
|                   1                   | 0          | 5\* (see below)   |
|                   2                   | 1          | 10                |
|                   3                   | 2          | 15                |
|                   4                   | 3          | 30                |
|                   5                   | 4          | 300 (5 hours)     |
|                   6                   | 5          | 1080 (18 hours)   |
|                   7                   | 6          | 1440 (24 hours)   |
|                   8                   | 7          | 1440 (24 hours    |

> 🚧 _Important_
> 
> _Once the webhook is suspended, it looses all its tracking data. For example, if a customer reactivates the webhook after one week, they loose one week of the tracking data. Therefore, if you do not want to loose any tracking data, then make sure to activate it promptly._

A list of possible error codes are explained in the following table. 

[block:parameters]
{
  "data": {
    "h-0": "Error  Code",
    "h-1": "Error description",
    "h-2": "Details",
    "0-0": "**400**",
    "0-1": "**Bad Request**",
    "0-2": "Occurs when the server cannot understand the request. This can happen when there is a simple error in the request.",
    "1-0": "**401**",
    "1-1": "**Unauthorized**",
    "1-2": "Occurs when the request was not successful as it lacks valid authentication credentials for the requested resource.",
    "2-0": "**402**",
    "2-1": "**Payment Required EXPERIMENTAL**",
    "2-2": "Occurs when the payment has not gone through. To resolve this, client must make a payment to access the requested resource.",
    "3-0": "**403**",
    "3-1": "**Forbidden** (Unauthorized)",
    "3-2": "Occurs when you do not have permission to access a web page or something else on a web server.",
    "4-0": "**410**",
    "4-1": "**Gone**",
    "4-2": "Occurs when the requested resource is permanently unavailable on the server. This is due to the resource that has been intentionally removed or retired and will not return.",
    "5-0": "**413**",
    "5-1": "**Payload Too Large**",
    "5-2": "Occurs when the size of the request exceeds the server’s file size limit.",
    "6-0": "**414**",
    "6-1": "**URL/URI Too Long**",
    "6-2": "Occurs when the requested URL (or URI) is longer than the server can interpret or process.",
    "7-0": "**415**",
    "7-1": "**Unsupported Media Type**",
    "7-2": "Occurs when the payload format is not supported by the server.",
    "8-0": "**416**",
    "8-1": "**Range Not Satisfiable**",
    "8-2": "Occurs when the partial range request sent by the client does not make sense for the given resource.",
    "9-0": "**417**",
    "9-1": "**Expectation Failed**",
    "9-2": "Occurs when the server or something in its response process does not support the conditions in the ‘Expect’ header.  \n  \nThis error indicates that the server could not do what was asked in the ‘Expect’ header of a request.",
    "10-0": "**418**",
    "10-1": "**I'm a teapot**",
    "10-2": "N/A",
    "11-0": "**501**",
    "11-1": "**Not Implemented**",
    "11-2": "Occurs when the web server does not support the facility required. This is not something you can resolve as it requires a fix from the web server admin.",
    "12-0": "**505**",
    "12-1": "**HTTP Version Not Supported**",
    "12-2": "Occurs when the server does not recognize or support the HTTP protocol version specified in the client’s request.",
    "13-0": "**506**",
    "13-1": "**Variant Also Negotiates**",
    "13-2": "Occurs when there is an issue with the server.",
    "14-0": "**510**",
    "14-1": "**Not Extended**",
    "14-2": "Occurs when the server requires additional extensions to fulfil a request.",
    "15-0": "**511**",
    "15-1": "**Network Authentication Required**",
    "15-2": "Occurs when the client's attempt to authenticate to gain network access fails."
  },
  "cols": 3,
  "rows": 16,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


> 💡 _Tip_
> 
> _It is a good practice to have a dedicated monitoring for the webhook so that you can be notified when it starts returning the errors. _