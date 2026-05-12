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

> 🚧 _Important_
>
> _Once the webhook is suspended, it looses all its tracking data. For example, if a customer reactivates the webhook after one week, they loose one week of the tracking data. Therefore, if you do not want to loose any tracking data, then make sure to activate it promptly._

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
  4. **Notification**: An email is sent to the user registered to receive the suspension notifications. This email can be specified while [configuring the Webhook details](https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook).
  5. **Retry Loop**: When the webhook is suspended, it will be queued to retry again.
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
  |     7    |      6      | 72 hours    |
  |     8    |      7      | 72 hours    |
</Accordion>

<Accordion title="Reactivation Process" icon="power-off">
  To reactivate a suspended webhook:

  1. Navigate to the webhook configuration in your GUI
  2. Toggle the **Activate** switch to enable the webhook
  3. Monitor the endpoint to ensure it's functioning properly

  <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" alt="Activating tracking webhook" />
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

<Cards columns="3">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>
</Cards>
