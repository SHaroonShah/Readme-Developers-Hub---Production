---
title: DX Rate Limiting
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
The DX carrier integration has it's own specific rate limit of **20 API requests per minute**. This impacts the [Create Shipment ](https://api.test.intersoftsapient.net/docs/v4-DX/api/index.html#tag/Shipments/paths/~1v4~1shipments~1DX/post)endpoint when creating DX shipping labels. 

The DX rate limit is set for all connections between Intersoft and the <<glossary:carrier>> for all activities relating to processing a <<glossary:shipment>>, including tracking which is requested in the background and therefore might impact the rate limit. 

This is the standard rate limit that DX has created, however based on your DX shipping profile the limit might be increased. If you have any questions regarding your DX rate limit, please reach out to your DX account manager.

> 🚧 _Important_
> 
> _If the DX rate limit is reached you will get the **503 Service Unavailable** error as shown in the following figure_. 
> 
> [block:image]{"images":[{"image":["https://files.readme.io/141c03f-image.png",null,"Displaying 503 error message"],"align":"center","border":true,"caption":"Displaying 503 error message"}]}[/block]

## See also

- [Intersoft API rate limiting](https://docs.intersoftsapient.net/docs/api-rate-limiting)