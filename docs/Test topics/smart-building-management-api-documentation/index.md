---
title: Smart Building Management API Documentation
deprecated: false
hidden: true
icon: fad fa-warehouse
metadata:
  robots: index
---
# <br />Introduction

This section helps you understand on how to integrate with the fictional Smart Building Management REST API to monitor building data, control devices, and automate workflows.

## API scope

The API supports applications and third-party integrations for building devices, including HVAC systems, lighting, occupancy sensors, energy meters, and alarms.

You can retrieve live building data, manage equipment, automate workflows, and connect smart-building functionality to external platforms.

## Who should use this documentation

<Columns layout="auto">
  <Column>

### Primary audiences

- Software developers
- API integrators
- Solution architects
- Technical consultants
- QA engineers

  </Column>
  <Column>

### Start with this knowledge

- Work with REST APIs.
- Use HTTP methods: `GET`, `POST`, `PUT`, and `DELETE`.
- Read and write JSON.
- Access your API credentials.
- Run requests with Postman, cURL, or a programming language that can make HTTP requests.

  </Column>
</Columns>

## Integration goals

<Columns layout="auto">
  <Column>

### What you can do

- Generate API credentials.
- Authenticate with OAuth 2.0.
- Make authenticated API requests.
- Retrieve building information and sensor data.
- Control building devices.
- Handle common API errors and troubleshoot request failures.

  </Column>
  <Column>

### Problems this documentation addresses

Smart building platforms can expose hundreds of endpoints. This documentation helps you authenticate successfully, find available endpoints, interpret API responses, troubleshoot integrations, and keep implementation guidance aligned with product updates.

  </Column>
</Columns>

## API requirements and limitations

Use an internet connection and HTTPS for every request. The API uses OAuth 2.0 authentication and JSON request and response bodies.

This documentation covers API version `v1`.

<br />
