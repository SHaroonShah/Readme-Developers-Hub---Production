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

> 🚧 _Important_
>
> _Once the webhook is suspended, it looses all its tracking data. For example, if a customer reactivates the webhook after one week, they loose one week of the tracking data. Therefore, if you do not want to loose any tracking data, then make sure to activate it promptly._

***

## Error reference

<Accordion title="Common Error Codes" icon="bug">
  Understanding these error codes can help you troubleshoot webhook issues:

  <Tabs>
    <Tab title="Client Errors (4xx)">
      | Error Code | Description                | Details                                                    |
      | :--------: | :------------------------- | :--------------------------------------------------------- |
      |   **400**  | **Bad Request**            | Server cannot understand the request due to client error   |
      |   **401**  | **Unauthorized**           | Request lacks valid authentication credentials             |
      |   **402**  | **Payment Required**       | Payment required to access the resource (experimental)     |
      |   **403**  | **Forbidden**              | No permission to access the resource                       |
      |   **410**  | **Gone**                   | Resource permanently unavailable and intentionally removed |
      |   **413**  | **Payload Too Large**      | Request size exceeds server's file size limit              |
      |   **414**  | **URL Too Long**           | Requested URL exceeds server processing limits             |
      |   **415**  | **Unsupported Media Type** | Payload format not supported by server                     |
      |   **416**  | **Range Not Satisfiable**  | Partial range request doesn't make sense for resource      |
      |   **417**  | **Expectation Failed**     | Server cannot meet 'Expect' header conditions              |
      |   **418**  | **I'm a teapot**           | Easter egg status code (not used in practice)              |
    </Tab>

    <Tab title="Server Errors (5xx)">
      | Error Code | Description                         | Details                                             |
      | :--------: | :---------------------------------- | :-------------------------------------------------- |
      |   **501**  | **Not Implemented**                 | Server doesn't support the required facility        |
      |   **505**  | **HTTP Version Not Supported**      | Server doesn't recognize the HTTP protocol version  |
      |   **506**  | **Variant Also Negotiates**         | Server configuration issue                          |
      |   **510**  | **Not Extended**                    | Server requires additional extensions               |
      |   **511**  | **Network Authentication Required** | Client authentication to gain network access failed |
    </Tab>
  </Tabs>
</Accordion>

***

## Best Practices

### Prevention

* Implement robust error handling
* Set up monitoring and alerting
* Ensure endpoint reliability
* Test webhook endpoints regularly

### Recovery

* Monitor suspension notifications
* Reactivate webhooks promptly
* Verify endpoint functionality
* Check for missed tracking data

***

### See also

<br />

<Cards columns="3">
  <Card title="Add Tracking Webhook" href="https://docs.intersoftsapient.net/docs/create-tracking-webhook" icon="fa-solid fa-calendar-circle-plus">
    Configure your webhook endpoint to receive tracking data.
  </Card>

  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>
</Cards>
