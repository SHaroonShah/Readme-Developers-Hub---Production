---
title: Troubleshooting API issues
excerpt: >-
  _Troubleshooting_ is a systematic process for identifying, diagnosing, and
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
    * **Adhere to required formats**: Ensure API requests follow the correct format (JSON, XML, and so on.)
    * **Refer to documentation**: Consult API references for proper usage and expected responses
  </Column>
</Columns>

***

# Troubleshooting at Intersoft

While using the system, if you run into any issues that you are unable to resolve or troubleshoot, provide the following information to expedite resolution:

<Accordion title="Information Required for Support Requests" icon="">
  <Cards columns="2">
    <Card title="Basic Information" icon="fa-solid fa-circle-info">
      * Customer name
      * Brief description of the issue and affected system areas
      * Issue severity level
      * Screenshots (if applicable)
    </Card>

    <Card title="Technical Details" icon="fa-solid fa-tachograph-digital">
      * Shipping location and/or shipping account details (ID or Alias)
      * Affected carriers
      * Date/time when the issue occurred
    </Card>

    <Card title="Tracking-Specific Info" icon="fa-solid fa-calendar-clock">
      * Example tracking numbers (for tracking-related issues)
      * Specify if tracking numbers are from Intersoft Sapient system OR registered via /trackings API
    </Card>

    <Card title="API Details" icon="fa-solid fa-code">
      * Store Intersoft format JSON request and response
      * Relevant error codes or messages
      * API endpoint information
    </Card>
  </Cards>

  <br />

  > 🚧 *Important*
  >
  > *Before sending us the request, please be aware of the following:*
  >
  > * *Do not send your Intersoft Sapient Client ID or Secret.*
  > * *Store the Intersoft format of the JSON request and response to allow us to investigate any API related issues.*

  If the issue you are experiencing is not outlined in the preceding cards or you do not have all the information on the issue, please reach out to our Tech Support team and provide all the necessary details of the issue to escalate the process.
</Accordion>

## Intersoft Tech Support contact details

Please use any of the following contact details to reach out to our Technical Support team:

<Columns layout="auto">
  <Column>
    > **Primary Contact Methods**

    📋 **Raise a Ticket**: [Intersoft Customer Portal](https://intersoftuk-servicedesk.atlassian.net/servicedesk/customer/portal/1?utm_source=hs_email\&utm_medium=email&_hsenc=p2ANqtz--Rf9pAocdpFBSK4Gjy9bwkO0ltWcb7apBqIoY-ugKNNGZaGP1BKnxqPBRddJlJY6Es78Fu)

    ✉️ **Email**: [TechSupport@intersoft.co.uk](mailto:TechSupport@intersoft.co.uk)

    📞 **Phone**: (+44) 01753 689 292
  </Column>

  <Column>
    > **Alternative Ticketing Domains**

    For seamless interaction with our support team, you can also use:

    * intersoftuk.atlassian.net
    * intersoftuk-servicedesk.atlassian.net
  </Column>
</Columns>