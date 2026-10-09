---
title: Shipment lifecycle and best practices
excerpt: >-
  Shipment creation is the starting point of the SAPIENT shipment workflow.
  During shipment creation, the selected shipment action determines how the
  shipment is processed, what information is returned in the response, and
  whether additional API calls are required before manifesting.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
A shipment can move through several stages between creation and manifesting, depending on how it was created and whether any additional processing actions are required. Understanding this lifecycle helps you use the correct APIs at the appropriate time, reduce unnecessary API calls, and ensure shipments are processed efficiently.

This guide explains the recommended SAPIENT shipment workflow, from creating a shipment and handling labels through to manifesting and carrier handover. It also covers common shipment management actions, including holding, releasing, cancelling, and recalling shipments, and highlights best practices to help you avoid common implementation mistakes.

Follow the recommended SAPIENT shipment lifecycle from shipment creation through label generation and manifesting. These guides explain when to use each shipment action, when the Print Label endpoint is required, and how to cancel, recall, hold or release one or multiple shipments efficiently.

Use this guide to:

- Understand the complete shipment lifecycle in SAPIENT.
- Choose the most appropriate shipment creation action (Process, Allocate, or Create).
- Determine when the Print Label API is required and when it is not.
- Manage shipment statuses throughout the processing workflow.
- Process multiple shipments more efficiently where supported.
- Ensure shipments are ready for manifesting and carrier collection.
