---
title: Webhooks
excerpt: >-
  _Webhooks_ are valuable tools for receiving real-time updates and data from
  various services and applications. They allow you to automate workflows,
  integrate systems, and stay up to date on important events.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The application sending the data sends a **POST** API call containing the data to the receiving application​. The endpoint is hosted by the application receiving the data, not the application sending the data as with a request and response-based API​.

INTERSOFT offers a comprehensive <<glossary:tracking webhook>> solution for receiving tracking events from carriers. The tracking data is sent to the customer’s endpoint configured in the tracking webhook setup.

With this solution, you can track:  

- All <<glossary:shipments>> created on SAPIENT
- Specific shipments created on Intelligent Shipper  
- Royal Mail shipments created on any external shipping platform or by individuals

***

In this section, learn how to: 

- [Create tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook)
- [Set up tracking account](https://docs.intersoftsapient.net/docs/create-tracking-account)
- [Set up manifest webhook](https://docs.intersoftsapient.net/docs/manifest-webhook)
- [Track events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones)
- [View webhook suspension codes](https://docs.intersoftsapient.net/docs/webhook-suspension)