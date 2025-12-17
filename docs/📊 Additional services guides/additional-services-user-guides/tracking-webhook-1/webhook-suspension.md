---
title: Webhook suspension
excerpt: >-
  _Webhook suspension_ refers to the disabling of the webhook notifications for
  shipment events due to an error.
deprecated: false
hidden: false
icon: fad fa-file-circle-minus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

Webhook suspension refers to the disabling of webhook notifications for shipment events due to errors. When the receiving endpoint encounters issues like timeouts or invalid data, SAPIENT may suspend notifications to prevent system overload.

<Cards columns={2}>
  <Card title="Quick Recovery" icon="bolt">
    Reactivate suspended webhooks immediately using the **Activate** toggle in the GUI to minimize data loss.
  </Card>
  <Card title="Monitoring Setup" icon="chart-line">
    Set up dedicated webhook monitoring before suspension notifications are triggered for better reliability.
  </Card>
</Cards>

## How Webhook Suspension Works

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

| Retry ID | Retry Count | Interval |
|:--------:|:-----------:|:---------|
| 1 | 0 | 5 minutes* |
| 2 | 1 | 10 minutes |
| 3 | 2 | 15 minutes |
| 4 | 3 | 30 minutes |
| 5 | 4 | 5 hours |
| 6 | 5 | 18 hours |
| 7 | 6 | 24 hours |
| 8 | 7 | 24 hours |

*Initial retry after first failure

</Accordion>

<Accordion title="Reactivation Process" icon="power-off">

To reactivate a suspended webhook:

1. Navigate to the webhook configuration in your GUI
2. Toggle the **Activate** switch to enable the webhook
3. Monitor the endpoint to ensure it's functioning properly

<Image align="center" alt="Activating tracking webhook" border={true} caption="Activating tracking webhook" src="https://files.readme.io/a76feb6-image.png" width="660px" />

</Accordion>

## Important Considerations

<Cards columns={1}>
  <Card title="Data Loss Warning" icon="exclamation-triangle">
    **Critical**: Once suspended, webhooks lose all tracking data accumulated during the suspension period. For example, reactivating after one week means losing one week of tracking data. Activate promptly to minimize data loss.
  </Card>
</Cards>

## Error Reference

<Accordion title="Common Error Codes" icon="bug">

Understanding these error codes can help you troubleshoot webhook issues:

<Tabs>
  <Tab title="Client Errors (4xx)">
  
| Error Code | Description | Details |
|:----------:|:------------|:---------|
| **400** | **Bad Request** | Server cannot understand the request due to client error |
| **401** | **Unauthorized** | Request lacks valid authentication credentials |
| **402** | **Payment Required** | Payment required to access the resource (experimental) |
| **403** | **Forbidden** | No permission to access the resource |
| **410** | **Gone** | Resource permanently unavailable and intentionally removed |
| **413** | **Payload Too Large** | Request size exceeds server's file size limit |
| **414** | **URL Too Long** | Requested URL exceeds server processing limits |
| **415** | **Unsupported Media Type** | Payload format not supported by server |
| **416** | **Range Not Satisfiable** | Partial range request doesn't make sense for resource |
| **417** | **Expectation Failed** | Server cannot meet 'Expect' header conditions |
| **418** | **I'm a teapot** | Easter egg status code (not used in practice) |

  </Tab>
  <Tab title="Server Errors (5xx)">
  
| Error Code | Description | Details |
|:----------:|:------------|:---------|
| **501** | **Not Implemented** | Server doesn't support the required facility |
| **505** | **HTTP Version Not Supported** | Server doesn't recognize the HTTP protocol version |
| **506** | **Variant Also Negotiates** | Server configuration issue |
| **510** | **Not Extended** | Server requires additional extensions |
| **511** | **Network Authentication Required** | Client authentication to gain network access failed |

  </Tab>
</Tabs>

</Accordion>

## Best Practices

### Prevention
- Implement robust error handling
- Set up monitoring and alerting
- Ensure endpoint reliability
- Test webhook endpoints regularly

### Recovery
- Monitor suspension notifications
- Reactivate webhooks promptly
- Verify endpoint functionality
- Check for missed tracking data