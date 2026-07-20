---
title: Introduction
excerpt: >-
  Integrate Smart Building Management API capabilities, including live sensor
  data, HVAC monitoring, lighting control, alarms, occupancy, and energy
  consumption.
deprecated: false
hidden: false
icon: fad fa-warehouse
metadata:
  robots: index
---
# Introduction

Use the Smart Building Management API to integrate building systems with your custom applications.

## What you can do

The API follows REST principles and exchanges JSON over HTTPS. Use it to access operational data and control connected building systems.

<Columns layout="auto">
  <Column>

### Monitor your building

- Retrieve live sensor data
- Monitor HVAC systems
- Access occupancy information
- Track energy consumption

  </Column>
  <Column>

### Manage building systems

- Control lighting
- Manage alarms

  </Column>
</Columns>

<br />

## Documentation structure

Use these sections as you build your integration:

- **Quick Start** — Get up and running quickly.
- **Authentication** — Secure API access.
- **API Reference** — Review endpoint details.

## API conventions

<Columns layout="auto">
  <Column>

### Base URL

[https://api.smartbuilding.example.com/v1](https://api.smartbuilding.example.com/v1)

  </Column>
  <Column>

### Response format

All responses are returned as JSON.

  </Column>
</Columns>

<br />

<Columns layout="auto">
  <Column>

### Authentication

Every request requires a Bearer token.

  </Column>
  <Column>

### Versioning

This documentation covers API version 1.

  </Column>
</Columns>

<Callout icon="circle-info" theme="info">
  Include a Bearer token with every request to authenticate with the API.
</Callout>