---
title: Sandbox vs Production account
excerpt: >-
  Learn the differences between SAPIENT's Sandbox and Production environments,
  including their purposes, features, and when to use each for testing and live
  shipping operations.
deprecated: false
hidden: false
icon: fad fa-viruses
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Understanding Sandbox vs Production Environments

Sandbox and Production are two different instances in software development and deployment, each serving distinct purposes in the SAPIENT platform.

<Cards columns={2}>
  <Card title="Sandbox Environment" icon="flask">
    A **testing environment** that simulates the production environment but is isolated from real-world operations.
    
    **Purpose:**
    - Experiment and develop safely
    - Test applications without affecting live systems
    - Identify bugs and issues
    - Experiment with new features
    
    **In SAPIENT:**
    - Provided during initial onboarding
    - Create test labels
    - Familiarize yourself with the system
    - Test your API credentials
  </Card>
  
  <Card title="Production Environment" icon="rocket">
    The **live setup** where applications operate and are accessible to end users and customers.
    
    **Purpose:**
    - Provide stable, secure, and reliable service
    - Handle real customer transactions
    - Process actual shipments
    
    **In SAPIENT:**
    - Access provided after onboarding completion
    - Official shipping and label creation
    - Live carrier integrations
    - Billable shipments
  </Card>
</Cards>

## Your SAPIENT Journey

<Columns layout="auto">
  <Column>
    ### 1. Onboarding Phase
    During your initial onboarding, you receive access to the **Sandbox** account. This is your safe testing ground where you can:
    - Learn the system without consequences
    - Create test labels
    - Validate your API integration
    - Practice with different shipping scenarios
  </Column>
  <Column>
    ### 2. Going Live
    Once you complete onboarding, you're ready for the **Production** environment where you can:
    - Create official shipments
    - Process real customer orders
    - Access live carrier services
    - Generate billable labels
  </Column>
</Columns>

<Accordion title="Important Warning" icon="exclamation-triangle">
**Always be aware of what account you are logged into.**

Any shipments accidentally created in the **Production** account are counted as live shipments. This means:
- They are created with the carrier as actual shipments
- You may be billed for these shipments
- They cannot be easily reversed

Double-check your environment before creating any shipments to avoid unexpected charges.
</Accordion>