---
title: Handle webhook suspension
excerpt: >-
  _Webhook suspension_ refers to the disabling of the webhook notifications for
  shipment events due to an error.
deprecated: false
hidden: false
icon: fad fa-file-circle-minus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If the receiving endpoint (the system where the notifications are sent) is down or encounters errors, for example, time out, invalid data, SAPIENT may suspend sending further webhook notifications to avoid overwhelming the system.

<Cards columns={2}>
  <Card title="Quick Recovery" icon="bolt">
    Reactivate suspended webhooks immediately using the **Activate** toggle in the GUI to minimise data loss.
  </Card>

  <Card title="Monitoring Setup" icon="chart-line">
    Set up dedicated webhook monitoring before suspension notifications are triggered for better reliability.
  </Card>
</Cards>

## How webhook suspension works

<Accordion title="Suspension Process" icon="pause-circle">
  When your webhook endpoint is down or encounters errors, SAPIENT follows a structured retry process before suspending the webhook:

  1. **Error Detection**: The system detects issues like timeouts, invalid data, or server errors
  2. **Retry Attempts**: Multiple retry attempts are made following specific intervals
  3. **Threshold Exceeded**: If all retry attempts fail, the webhook is suspended
  4. **Notification**: An email is sent to the primary user registered for the customer

  > **Primary User**: Set up during customer onboarding. Contact Intersoft's onboarding team to change the primary user.
</Accordion>

<Accordion title="Retry Schedule" icon="clock">
  The system follows this retry schedule before suspending a webhook:

  | Retry ID | Retry Count | Interval    |
  | :------: | :---------: | :---------- |
  |     1    |      0      | 5 minutes\* |
  |     2    |      1      | 10 minutes  |
  |     3    |      2      | 15 minutes  |
  |     4    |      3      | 30 minutes  |
  |     5    |      4      | 5 hours     |
  |     6    |      5      | 18 hours    |
  |     7    |      6      | 24 hours    |
  |     8    |      7      | 24 hours    |

  \*Initial retry after first failure
</Accordion>

<Accordion title="Reactivation Process" icon="power-off">
  To reactivate a suspended webhook:

  1. Navigate to the webhook configuration in your GUI
  2. Toggle the **Activate** switch to enable the webhook
  3. Monitor the endpoint to ensure it's functioning properly

  <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" alt="Activating tracking webhook" />

  <br />
</Accordion>

<br />

<Callout icon="💡" theme="default">
  ### _Tip_

  _To avoid webhook suspension, we highly recommend setting up a dedicated webhook monitoring system before the suspension notification is triggered. If the webhook does get suspended, you can[reactivate](https://docs.intersoftsapient.net/docs/create-tracking-webhook) it by enabling the **Activate** toggle in the GUI._

  <Image align="center" alt="Activating tracking webhook" border={true} caption="Activating tracking webhook" src="https://files.readme.io/a76feb6-image.png" width="660px" />
</Callout>

The retry intervals for the webhook are provided in the following table.

| ShipmentTrackingStatusRetryIntervalId | RetryCount | IntervalInMinutes |
| :-----------------------------------: | :--------- | :---------------- |
|                   1                   | 0          | 5* (see below)    |
|                   2                   | 1          | 10                |
|                   3                   | 2          | 15                |
|                   4                   | 3          | 30                |
|                   5                   | 4          | 300 (5 hours)     |
|                   6                   | 5          | 1080 (18 hours)   |
|                   7                   | 6          | 1440 (24 hours)   |
|                   8                   | 7          | 1440 (24 hours)   |

> 🚧 _Important_
>
> _Once the webhook is suspended, it looses all its tracking data. For example, if a customer reactivates the webhook after one week, they loose one week of the tracking data. Therefore, if you do not want to loose any tracking data, then make sure to activate it promptly._

A list of possible error codes are explained in the following table.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Error  Code
      </th>

      <th>
        Error description
      </th>

      <th>
        Details
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **400**
      </td>

      <td>
        **Bad Request**
      </td>

      <td>
        Occurs when the server cannot understand the request. This can happen when there is a simple error in the request.
      </td>
    </tr>

    <tr>
      <td>
        **401**
      </td>

      <td>
        **Unauthorized**
      </td>

      <td>
        Occurs when the request was not successful as it lacks valid authentication credentials for the requested resource.
      </td>
    </tr>

    <tr>
      <td>
        **402**
      </td>

      <td>
        **Payment Required EXPERIMENTAL**
      </td>

      <td>
        Occurs when the payment has not gone through. To resolve this, client must make a payment to access the requested resource.
      </td>
    </tr>

    <tr>
      <td>
        **403**
      </td>

      <td>
        **Forbidden**
        (Unauthorized)
      </td>

      <td>
        Occurs when you do not have permission to access a web page or something else on a web server.
      </td>
    </tr>

    <tr>
      <td>
        **410**
      </td>

      <td>
        **Gone**
      </td>

      <td>
        Occurs when the requested resource is permanently unavailable on the server. This is due to the resource that has been intentionally removed or retired and will not return.
      </td>
    </tr>

    <tr>
      <td>
        **413**
      </td>

      <td>
        **Payload Too Large**
      </td>

      <td>
        Occurs when the size of the request exceeds the server’s file size limit.
      </td>
    </tr>

    <tr>
      <td>
        **414**
      </td>

      <td>
        **URL/URI Too Long**
      </td>

      <td>
        Occurs when the requested URL (or URI) is longer than the server can interpret or process.
      </td>
    </tr>

    <tr>
      <td>
        **415**
      </td>

      <td>
        **Unsupported Media Type**
      </td>

      <td>
        Occurs when the payload format is not supported by the server.
      </td>
    </tr>

    <tr>
      <td>
        **416**
      </td>

      <td>
        **Range Not Satisfiable**
      </td>

      <td>
        Occurs when the partial range request sent by the client does not make sense for the given resource.
      </td>
    </tr>

    <tr>
      <td>
        **417**
      </td>

      <td>
        **Expectation Failed**
      </td>

      <td>
        Occurs when the server or something in its response process does not support the conditions in the ‘Expect’ header.

        This error indicates that the server could not do what was asked in the ‘Expect’ header of a request.
      </td>
    </tr>

    <tr>
      <td>
        **418**
      </td>

      <td>
        **I'm a teapot**
      </td>

      <td>
        N/A
      </td>
    </tr>

    <tr>
      <td>
        **501**
      </td>

      <td>
        **Not Implemented**
      </td>

      <td>
        Occurs when the web server does not support the facility required. This is not something you can resolve as it requires a fix from the web server admin.
      </td>
    </tr>

    <tr>
      <td>
        **505**
      </td>

      <td>
        **HTTP Version Not Supported**
      </td>

      <td>
        Occurs when the server does not recognize or support the HTTP protocol version specified in the client’s request.
      </td>
    </tr>

    <tr>
      <td>
        **506**
      </td>

      <td>
        **Variant Also Negotiates**
      </td>

      <td>
        Occurs when there is an issue with the server.
      </td>
    </tr>

    <tr>
      <td>
        **510**
      </td>

      <td>
        **Not Extended**
      </td>

      <td>
        Occurs when the server requires additional extensions to fulfil a request.
      </td>
    </tr>

    <tr>
      <td>
        **511**
      </td>

      <td>
        **Network Authentication Required**
      </td>

      <td>
        Occurs when the client's attempt to authenticate to gain network access fails.
      </td>
    </tr>
  </tbody>
</Table>
