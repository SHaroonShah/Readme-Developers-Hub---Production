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

If the threshold value for retrying the webhook within the given intervals is exceeded, then the webhook is suspended and a corresponding email is sent to the primary user registered for the customer. A *primary user* is set up at the time of customer onboarding. If you want to change the primary user, you can contact Intersoft's onboarding team.

> 💡 *Tip*
>
> *The webhook can be[activated](https://docs.intersoftsapient.net/docs/create-tracking-webhook) via the GUI.*

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

> 🚧 *Important*
>
> *Once the webhook is suspended, it looses all its tracking data. For example, if a customer reactivates the webhook after one week, they loose one week of the tracking data. Therefore, if you do not want to loose any tracking data, then make sure to activate it promptly.*

A list of possible error codes are explained in the following table. 

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Error  Code
      </th>

      <th style={{ textAlign: "left" }}>
        Error description
      </th>

      <th style={{ textAlign: "left" }}>
        Details
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        **400**
      </td>

      <td style={{ textAlign: "left" }}>
        **Bad Request**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the server cannot understand the request. This can happen when there is a simple error in the request.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **401**
      </td>

      <td style={{ textAlign: "left" }}>
        **Unauthorized**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the request was not successful as it lacks valid authentication credentials for the requested resource.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **402**
      </td>

      <td style={{ textAlign: "left" }}>
        **Payment Required EXPERIMENTAL**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the payment has not gone through. To resolve this, client must make a payment to access the requested resource.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **403**
      </td>

      <td style={{ textAlign: "left" }}>
        * \*Forbidden\*\* (Unauthorized)
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when you do not have permission to access a web page or something else on a web server.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **410**
      </td>

      <td style={{ textAlign: "left" }}>
        **Gone**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the requested resource is permanently unavailable on the server. This is due to the resource that has been intentionally removed or retired and will not return.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **413**
      </td>

      <td style={{ textAlign: "left" }}>
        **Payload Too Large**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the size of the request exceeds the server’s file size limit.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **414**
      </td>

      <td style={{ textAlign: "left" }}>
        **URL/URI Too Long**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the requested URL (or URI) is longer than the server can interpret or process.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **415**
      </td>

      <td style={{ textAlign: "left" }}>
        **Unsupported Media Type**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the payload format is not supported by the server.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **416**
      </td>

      <td style={{ textAlign: "left" }}>
        **Range Not Satisfiable**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the partial range request sent by the client does not make sense for the given resource.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **417**
      </td>

      <td style={{ textAlign: "left" }}>
        **Expectation Failed**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the server or something in its response process does not support the conditions in the ‘Expect’ header.  

        This error indicates that the server could not do what was asked in the ‘Expect’ header of a request.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **418**
      </td>

      <td style={{ textAlign: "left" }}>
        **I'm a teapot**
      </td>

      <td style={{ textAlign: "left" }}>
        N/A
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **501**
      </td>

      <td style={{ textAlign: "left" }}>
        **Not Implemented**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the web server does not support the facility required. This is not something you can resolve as it requires a fix from the web server admin.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **505**
      </td>

      <td style={{ textAlign: "left" }}>
        **HTTP Version Not Supported**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the server does not recognize or support the HTTP protocol version specified in the client’s request.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **506**
      </td>

      <td style={{ textAlign: "left" }}>
        **Variant Also Negotiates**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when there is an issue with the server.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **510**
      </td>

      <td style={{ textAlign: "left" }}>
        **Not Extended**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the server requires additional extensions to fulfil a request.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>
        **511**
      </td>

      <td style={{ textAlign: "left" }}>
        **Network Authentication Required**
      </td>

      <td style={{ textAlign: "left" }}>
        Occurs when the client's attempt to authenticate to gain network access fails.
      </td>
    </tr>
  </tbody>
</Table>

> 💡 *Tip*
>
> *It is a good practice to have a dedicated monitoring for the webhook so that you can be notified when it starts returning the errors.*
