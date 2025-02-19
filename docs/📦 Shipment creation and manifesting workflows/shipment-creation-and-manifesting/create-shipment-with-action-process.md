---
title: Create shipment with Process action
excerpt: >-
  _Process_ is an action that finalises the shipment creation and prepares the
  shipment for transportation.
deprecated: false
hidden: false
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

<Image alt="Workflow for creating shipments with the Process action" align="center" src="https://files.readme.io/f762106c6e0adca64fd03cbc168faecdddceccf9adcb67b8bb963988cc3090bc-Process_flow.png">
  Workflow for creating shipments with Process action
</Image>
