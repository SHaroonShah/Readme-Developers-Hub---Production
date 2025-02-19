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
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Benefits of setting rate limits

Setting up a rate limit has many benefits, but the most primary ones include the following:

- **Preventing system abuse**: rate limiting helps protect the API from malicious users, bots, or applications that may overwhelm the server with excessive requests.
- **Maintaining performance**: by controlling the flow of requests, rate limiting helps maintain the overall performance and responsiveness of the API for all users.
- **Resource management**: rate limiting aids in managing and shifting server resources to prevent overloading, which could eventually lead to poor performance or service outages.

## Role of TPS in rate limiting

_Transactions per second_ or _TPS_ is a performance metric used to measure the number of requests that an application can handle in one second. This is crucial for understanding the capacity and performance capabilities of the software’s API.

Moreover, knowing the TPS helps in predicting the number of users or transactions the API can handle concurrently. Specially, for the carrier management platforms, it can establish a baseline for testing the API under various conditions to ensure it can cope up with anticipated traffic peaks, such as Christmas, new year, and other peak days.

## Rate limiting ineffectiveness

If rate limiting is not appropriately configured or enforced, it may fail to throttle excessive users effectively leading to the following issues:

- Performance degradation
- Service outages
- Data integrity issues
- Increased cost
- Security vulnerability
- Coordination challenges at peak times

## Handling rate limits

Rate limits can be handled by both client and the server. For you to handle your rate limits, it is highly recommended to follow the best practises outlined in this section. By following these best practices, you can efficiently manage API rate limiting, reduce the risk of hitting limits, and ensure smoother interactions with the API, leading to a better user experience and improved application performance.

1. **Understand rate limits**: familiarize yourself with the API provider's rate limiting policies, including limits on requests per minute, hour, or day, as well as any specific rules related to your account type.

2. **Monitor API usage**: it is recommended to regularly check the number of requests made and the remaining calls to prevent hitting the limits unexpectedly. 

3. **Implement backoff**: develop a logic that progressively waits longer before retrying requests when rate limits are approached.

4. **Batch API calls**: if required, try to batch multiple requests into a single call to reduce the total number of requests made.

5. **Prioritise requests**: determine which API requests are essential and prioritize them, especially during high-traffic periods or when nearing rate limits.

6. **Implement throttling**: build the throttling mechanism to limit the number of requests sent over a defined interval, reducing the likelihood of exceeding rate limits.

7. **Graceful degradation**: design your applications in a way that ensure that the API can still function at a reduced capacity rather than halting completely when the limits are reached.

8. **Test rate limiting behaviour**: during development, stimulate high volume requests to see how your application handles the rate limiting. Based on the results, improvise your strategies.

9. **Keep up with API changes**: stay informed regarding any updates from the API provider, such as changes to rate limits, best practices, or new features.

10. **Utilise status monitoring**: implement tools to monitor the API's health and response times, enabling you to adjust your request rates proactively if the API is experiencing high load.

# Intersoft rate limiting policy

Intersoft enforces limits on the API calls a customer can make based on their subscription settings. The limits apply to the use of the **CreateShipment** API.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/719a12c369c234e47811487ce0fd5676ff2279762a470472873b90f2f3066148-Throttling.png",
        "",
        "Throttling additional requests"
      ],
      "align": "center",
      "sizing": "600px",
      "border": true,
      "caption": "Throttling additional requests"
    }
  ]
}
[/block]


Our rate limiting policy is designed to strike a balance between providing access to our services and ensuring their reliability and performance. It is a critical component of responsible API usage, and we appreciate your cooperation in adhering to the following limits. 

| Requests per 10 seconds | Transaction per second (TPS) | Notes                                       |
| :---------------------: | :--------------------------: | :------------------------------------------ |
|            60           |               6              | Default for all existing and new customers. |

> 📘 _Note_
> 
> _The rate limit mentioned in the preceding table is Intersoft specific. Some carriers may have their own rate limits and additional carrier limitations. If the existing rate limit do not fit your needs, please reach out to our customers solutions team. _

# Frequently asked questions (FAQs)

**How do I choose the right API rate limiting solution for my needs?**

To choose the right API rate limiting solution for your needs, you should consider factors such as the number of API calls you need to support, the level of security you require, and your budget.

**How much does a higher API TPS solution cost?**

The cost of a higher API TPS solution varies depending on the the number of API calls you need to support, and the level of support you require. However, as a general guideline, it is recommended to reach out to our sales team and discuss your requirements.

**How can I get started with an API rate limiting solution?**

To get started with an API rate limiting solution, you can contact our customer solutions team to discuss your specific needs and requirements. We will help you choose the right solution and provide you with the necessary support to get started.