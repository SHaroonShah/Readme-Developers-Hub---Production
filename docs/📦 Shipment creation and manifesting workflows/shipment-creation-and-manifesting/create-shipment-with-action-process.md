---
title: Create shipment with Process action
excerpt: >-
  _Process_ is an action that finalises the shipment creation and prepares the
  shipment for transportation.
deprecated: false
hidden: false
icon: fad fa-cart-minus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you want to create the <Glossary>shipments</Glossary> and print the <Glossary>labels</Glossary>, then use the **Process** action in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request. In this case, shipments are ready to be manifested at any time you want. Additionally, this action also reduces the number API calls you need to make.

If your warehouse simultaneously picks, packs and sticks labels to shipments, then, if required,  labels and <Glossary>CN23</Glossary> are returned in the successful response.

If no value is set for the **Create Shipment** action, then the shipments are  created with the **Process** status.

<Image align="center" alt="Workflow for creating shipments with the Process action" border={false} caption="Workflow for creating shipments with Process action" src="https://files.readme.io/f762106c6e0adca64fd03cbc168faecdddceccf9adcb67b8bb963988cc3090bc-Process_flow.png" />

To view a step-by-step process on how to process the shipments that are created with the action "Process," refer to the following API recipe:

<TutorialTile emoji="🦉" slug="process-shipments-created-with-the-action-process" title="Process shipment created with the action “Process”" />