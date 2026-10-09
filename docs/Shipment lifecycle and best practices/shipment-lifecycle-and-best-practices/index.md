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
Follow the recommended SAPIENT shipment workflow from authentication and shipment creation through label generation, status management and manifesting.

The action you select when creating a shipment determines how it is processed and whether you need further application programming interface (API) calls before manifesting. Use the guides below to choose an action, determine when to use the Print Label API, manage shipments and prepare them for carrier handover.

## Getting started

Start with authentication, then follow the shipment workflow in order. You can also open a specific guide when you need to manage a shipment or check whether it is ready to manifest.

<Cards>
  <Card title="Authentication best practices" href="/docs/authentication-best-practices" icon="fa-solid fa-key">
    Obtain a bearer token and use it to authenticate your API requests.
  </Card>
  <Card title="Shipment lifecycle" href="/docs/shipment-lifecycle" icon="fa-solid fa-route">
    Follow the stages from shipment creation to manifesting and carrier handover.
  </Card>
  <Card title="Shipment action and label decision flow" href="/docs/shipment-action-and-label-decision-flow" icon="fa-solid fa-tags">
    Choose a shipment action and determine when you need the Print Label API.
  </Card>
  <Card title="Manage shipment status flow" href="/docs/manage-shipment-status-flow" icon="fa- solid fa-arrows-rotate">
    Find the guidance for managing shipment statuses during processing.
  </Card>
  <Card title="Bulk status update flow" href="/docs/bulk-status-update-flow" icon="fa-solid fa-layer-group">
    Find the guidance for updating statuses across multiple shipments.
  </Card>
  <Card title="Manifest readiness flow" href="/docs/manifest-readiness-flow" icon="fa-solid fa-clipboard-check">
    Check the steps to take before manifesting shipments.
  </Card>
</Cards>