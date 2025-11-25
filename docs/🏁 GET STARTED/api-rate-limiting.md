---
title: API Rate Limiting
excerpt: >-
  Learn about API rate limiting, its benefits, and best practices for managing
  request limits to ensure optimal performance and security.
deprecated: false
hidden: false
icon: fad fa-transporter-7
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## What is API Rate Limiting?

Rate limiting controls the number of requests a client can make to an API within a specific timeframe (per second, minute, or hour). This prevents system abuse, maintains performance, and ensures fair resource allocation.

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

_Note: Some carriers may have additional rate limits beyond Intersoft's policy._

## Frequently Asked Questions

<Accordion title="What if I need a higher rate limit?">
  Contact our customer solutions team to discuss upgrading your rate limits. Additional carrier limitations may also apply.
</Accordion>

<Accordion title="How do I choose the right rate limiting solution?">
  Consider your API call volume, security requirements, and budget. Our sales team can help assess your specific needs.
</Accordion>

<Accordion title="What does a higher TPS solution cost?">
  Pricing varies based on call volume and support level required. Contact our sales team for custom pricing.
</Accordion>

<Accordion title="How do I get started?">
  Reach out to our customer solutions team to discuss your requirements and get the right solution configured.
</Accordion>

<ToggleList>
    <ToggleListItem title={<strong>What if I need a higher rate limit?</strong>}>
      Contact our customer solutions team to discuss upgrading your rate limits. Additional carrier limitations may also apply.
    </ToggleListItem>

    <ToggleListItem title={<strong>How do I choose the right rate limiting solution?</strong>}>
 Consider your API call volume, security requirements, and budget. Our sales team can help assess your specific needs.
    </ToggleListItem>

    <ToggleListItem title={<strong>What does a higher TPS solution cost?</strong>}>
      Pricing varies based on call volume and support level required. Contact our sales team for custom pricing.

  </ToggleListItem>   <ToggleListItem title={<strong>How do I get started?</strong>}>
 Reach out to our customer solutions team to discuss your requirements and get the right solution configured.
    </ToggleListItem>

  </ToggleList>

<br />
