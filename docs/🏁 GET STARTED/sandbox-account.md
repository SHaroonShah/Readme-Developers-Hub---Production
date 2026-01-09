---
title: Sandbox vs Production account
excerpt: >-
  Sandbox and Production are two different instances in software development and
  deployment, each serving different purposes.
deprecated: false
hidden: false
icon: fad fa-viruses
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Cards columns={2}>
  <Card title="Sandbox Environment" icon="fa-solid fa-flask">
    A **testing environment** that simulates the production environment but is isolated from real-world operations.

    **Purpose:**

    * Experiment and develop safely
    * Test applications without affecting live systems
    * Identify bugs and issues
    * Experiment with new features

    **In SAPIENT:**

    * Provided during initial onboarding
    * Create test labels
    * Familiarise yourself with the system
    * Test your API credentials
  </Card>

  <Card title="Production Environment" icon="fa-solid fa-conveyor-belt-arm">
    The **live setup** where applications operate and are accessible to end users and customers.

    **Purpose:**

    * Provide stable, secure, and reliable service
    * Handle real customer transactions
    * Process actual shipments

    **In SAPIENT:**

    * Access provided after onboarding completion
    * Official shipping and label creation
    * Live carrier integrations
    * Billable shipments
  </Card>
</Cards>

> 🚧 _Important_
>
> _Always be aware of what account you are logged into. Any shipments accidently created in the**Production** account are counted as live shipments. This means:_
>
> * _These shipments are created with the carrier as actual shipments_
> * _You may be billed for these shipments_
> * _These shipments cannot be reversed_
>
> _It is recommended to double-check your environment before creating any shipments to avoid unexpected charges._
