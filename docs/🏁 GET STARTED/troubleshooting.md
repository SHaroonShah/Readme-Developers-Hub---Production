---
title: Troubleshooting
excerpt: >-
  Comprehensive troubleshooting guide for API issues and Intersoft system
  support with best practices and contact information.
deprecated: false
hidden: false
icon: fad fa-screwdriver-wrench
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
<Accordion title="Common API Issues" icon="exclamation-triangle">

When troubleshooting API-related issues, it's important to first understand the problem. Here are the most common issues you might encounter:

<Cards columns="2">
  <Card title="Authentication Failures" icon="lock">
    Problems related to API keys, tokens, or user credentials that prevent access to the system.
  </Card>
  
  <Card title="Network Issues" icon="wifi">
    Connectivity problems that prevent the API from being reached or responding properly.
  </Card>
  
  <Card title="Rate Limiting" icon="tachometer-alt">
    Issues arising from hitting the maximum allowed number of requests per time period.
  </Card>
  
  <Card title="Request/Response Issues" icon="exchange-alt">
    Communication problems between API systems that can occur at either the request or response end.
  </Card>
  
  <Card title="Endpoint Problems" icon="plug">
    Issues specifically associated with API endpoints, including availability and configuration.
  </Card>
  
  <Card title="Tracking Issues" icon="search">
    Problems related to monitoring or recording interactions between client applications and APIs.
  </Card>
</Cards>

</Accordion>

<Accordion title="Best Practices for API Troubleshooting" icon="check-circle">

Follow these recommended practices to maintain functionality and prevent issues:

<Columns layout="auto">
  <Column>
    **Analysis & Monitoring**
    - **Analyze response errors**: Review HTTP status codes (400, 401, 429, 500) to understand failures
    - **Perform logging and monitoring**: Use logs to track API interactions and identify errors
    - **Check your rate limits**: Verify that request frequency stays within allowed limits
  </Column>
  
  <Column>
    **Testing & Documentation**
    - **Use testing tools**: Leverage tools like Postman or curl for manual API testing
    - **Adhere to required formats**: Ensure API requests follow the correct format (JSON, XML, etc.)
    - **Refer to documentation**: Consult API references for proper usage and expected responses
  </Column>
</Columns>

</Accordion>

## Troubleshooting Support at Intersoft

<Accordion title="Information Required for Support Requests" icon="list-ul">

When contacting Intersoft for troubleshooting assistance, please provide the following information to expedite resolution:

<Cards columns="2">
  <Card title="Basic Information" icon="info-circle">
    - Customer name
    - Brief description of the issue and affected system areas
    - Issue severity level
    - Screenshots (if applicable)
  </Card>
  
  <Card title="Technical Details" icon="cogs">
    - Shipping location and/or shipping account details (ID or Alias)
    - Affected carriers
    - Date/time when the issue occurred
  </Card>
  
  <Card title="Tracking-Specific Info" icon="shipping-fast">
    - Example tracking numbers (for tracking-related issues)
    - Specify if tracking numbers are from Intersoft Sapient system OR registered via /trackings API
  </Card>
  
  <Card title="API Details" icon="code">
    - Store Intersoft format JSON request and response
    - Relevant error codes or messages
    - API endpoint information
  </Card>
</Cards>

> 🚧 **Important Security Note**
>
> **Before sending your request:**
> - Do **NOT** send your Intersoft Sapient Client ID or Secret
> - Store the complete JSON request and response format to help with API issue investigation

</Accordion>

<Accordion title="Contact Intersoft Tech Support" icon="phone">

<Columns layout="auto">
  <Column>
    **Primary Contact Methods**
    
    📋 **Raise a Ticket**: [Intersoft Customer Portal](https://intersoftuk-servicedesk.atlassian.net/servicedesk/customer/portal/1?utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz--Rf9pAocdpFBSK4Gjy9bwkO0ltWcb7apBqIoY-ugKNNGZaGP1BKnxqPBRddJlJY6Es78Fu)
    
    ✉️ **Email**: [TechSupport@intersoft.co.uk](mailto:TechSupport@intersoft.co.uk)
    
    📞 **Phone**: (+44) 01753 689 292
  </Column>
  
  <Column>
    **Alternative Ticketing Domains**
    
    For seamless interaction with our support team, you can also use:
    
    - intersoftuk.atlassian.net
    - intersoftuk-servicedesk.atlassian.net
    
    > 💡 **Tip**: Using our internal ticketing system ensures faster response times and better issue tracking.
  </Column>
</Columns>

</Accordion>