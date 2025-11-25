---
title: Troubleshooting
excerpt: >-
  Troubleshooting is a systematic process for identifying, diagnosing, and
  resolving problems for issues. It involves investigating a malfunction or
  failure to ensure that system or process runs smoothly.
deprecated: false
hidden: false
icon: fad fa-screwdriver-wrench
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Common issues

When it comes to troubleshooting API related issues, it is important to first understand the issue. Here are some common API related issues that you might encounter during your processes:

|                Issue                | Description                                                                                      |
| :---------------------------------: | :----------------------------------------------------------------------------------------------- |
|     **Authentication failures***    | Problems related to API keys, tokens, or user credentials that prevent access to the system.     |
|          **Network issues**         | Connectivity problems that prevent the API from being reached or responding properly.            |
|          **Rate limiting**          | Issues arising from hitting the maximum allowed number of requests per time period.              |
| **API request and response issues** | Communication problems between API systems that can occur at either the request or response end. |
|      **Affected API endpoint**      | Issues specifically associated with API endpoints, including availability and configuration.     |
|         **Tracking issues**         | Problems related to monitoring or recording interactions between client applications and APIs.   |

***

## Best practises

For smooth interaction with the APIs it is recommended to follow some best practises to maintain the functionality and avoid issue generation.

<Accordion title="Recommended practises" icon="fa-info-circle">
  <Columns layout="auto">
    <Column>
      **Analysis & Monitoring**

      * **Analyze response errors**: Review HTTP status codes (400, 401, 429, 500) to understand failures
      * **Perform logging and monitoring**: Use logs to track API interactions and identify errors
      * **Check your rate limits**: Verify that request frequency stays within allowed limits
    </Column>

    <Column>
      **Testing & Documentation**

      * **Use testing tools**: Leverage tools like Postman or curl for manual API testing
      * **Adhere to required formats**: Ensure API requests follow the correct format (JSON, XML, etc.)
      * **Refer to documentation**: Consult API references for proper usage and expected responses
    </Column>
  </Columns>
</Accordion>

***

# Troubleshooting at Intersoft

While using the system, if you run into any issues that you are unable to resolve or troubleshoot, you can always contact Intersoft. This section lists the standard information for all requests that we will require from you to troubleshoot your issues.

* Customer name
* Brief description of the issue and what areas of the system are impacted (provide any screenshots necessary)
* Severity of the issue
* Shipping location and/or shipping accounts affected (ID or Alias)
* Affected carriers
* Examples of tracking numbers (for tracking-related issues)
* Advise if the tracking numbers belong to shipments that have been created on the Intersoft Sapient system OR if they have been registered via the /trackings API.
* Date/time of when the issue was generated

> 🚧 _Important_
>
> _Before sending us the request, please be aware of the following:_
>
> * _Do not send your Intersoft Sapient Client ID or Secret._
> * _Store the Intersoft format of the JSON request and response to allow us to investigate any API related issues._

If the issue you are experiencing is not outlined in the preceding list or you do not have all the information on the issue, please reach out to our Tech Support team and provide all the necessary details of the issue to escalate the process.

## Intersoft Tech Support contact details

Please use any of the following contact details to reach out to our Technical Support team:

**Raise a ticket**: [Intersoft Customer Portal](https://intersoftuk-servicedesk.atlassian.net/servicedesk/customer/portal/1?utm_source=hs_email\&utm_medium=email&_hsenc=p2ANqtz--Rf9pAocdpFBSK4Gjy9bwkO0ltWcb7apBqIoY-ugKNNGZaGP1BKnxqPBRddJlJY6Es78Fu)  
**Email**: [TechSupport@intersoft.co.uk](mailto:TechSupport@intersoft.co.uk)
**Phone**: (+44) 01753 689 292

<Callout icon="💡" theme="default">
  ### _Tip_

  _For seamless interaction with our support team, you may also raise your queries using any of the following domains of our internal ticketing system:_

  * _intersoftuk.atlassian.net_
  * _intersoftuk-servicedesk.atlassian.net_
</Callout>
