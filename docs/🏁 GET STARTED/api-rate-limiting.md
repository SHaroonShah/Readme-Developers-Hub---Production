---
title: API Rate Limiting
excerpt: >-
  _Rate limiting_ is a technique primarily used in APIs to control the number of
  requests or API calls a client can make to the server within a given span of
  time. This method of restricting the API calls is achieved by setting a
  threshold limit on the number of requests that can be processed over a
  specified time frame, for example, per second, per minute, or hour.
deprecated: false
hidden: false
icon: fad fa-transporter-7
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Key Benefits

* **Prevents abuse**: Protects against malicious users and bots overwhelming the server
* **Maintains performance**: Ensures consistent API responsiveness for all users
* **Resource management**: Prevents server overload and service outages

## Understanding TPS

_Transactions per Second (TPS)_ measures how many requests an API can handle per second. This metric helps:

* Determine system capacity and performance limits
* Predict concurrent user handling capabilities
* Establish baselines for peak traffic testing

## Best Practices for Handling Rate Limits

1. **Know your limits**: Understand the API's rate limiting policies and account-specific rules
2. **Monitor usage**: Track requests made and remaining quota to avoid unexpected limits
3. **Implement backoff**: Use exponential backoff when approaching rate limits
4. **Batch requests**: Combine multiple operations into single API calls when possible
5. **Prioritize critical requests**: Focus on essential API calls during high-traffic periods
6. **Build in throttling**: Limit outgoing request rates proactively
7. **Plan for degradation**: Design applications to function at reduced capacity when limits are reached
8. **Test thoroughly**: Simulate high-volume scenarios during development
9. **Stay updated**: Monitor API provider announcements for policy changes
10. **Monitor API health**: Use tools to track response times and adjust request rates accordingly

## Intersoft Rate Limiting Policy

Intersoft enforces limits on API calls based on subscription settings, specifically for the **CreateShipment** API.

<Image align="center" alt="Throttling additional requests" border={true} caption="Throttling additional requests" src="https://files.readme.io/719a12c369c234e47811487ce0fd5676ff2279762a470472873b90f2f3066148-Throttling.png" width="600px" />

| Requests per 10 seconds | TPS | Account Level              | Estimated Volume (1 hour/day, 20 days/month |
| :---------------------: | :-: | :------------------------- | :------------------------------------------ |
|            10           |  1  | Base product account level | 72k requests                                |

> 📘 _Note_
>
> _Some carriers may have additional rate limits beyond Intersoft's policy._

# Frequently asked questions (FAQs)

<Accordion title="What do I need to do if I need a higher rate limit?">
  The rate limit mentioned in the preceding table is Intersoft specific. Some carriers may have their own rate limits and additional carrier limitations. If you need a higher rate limit than the our existing one, please reach out to our customers solutions team.
</Accordion>

<Accordion title="How do I choose the right API rate limiting solution for my needs?">
  To choose the right API rate limiting solution for your needs, you should consider factors such as the number of API calls you need to support, the level of security you require, and your budget.
</Accordion>

<Accordion title="How much does a higher API TPS solution cost?">
  The cost of a higher API TPS solution varies depending on the the number of API calls you need to support, and the level of support you require. However, as a general guideline, it is recommended to reach out to our sales team and discuss your requirements.
</Accordion>

<Accordion title="How can I get started with an API rate limiting solution?">
  To get started with an API rate limiting solution, you can contact our customer solutions team to discuss your specific needs and requirements. We will help you choose the right solution and provide you with the necessary support to get started.
</Accordion>
