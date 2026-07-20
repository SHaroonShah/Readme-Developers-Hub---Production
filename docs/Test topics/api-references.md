---
title: API references
excerpt: >-
  This section provides you with the relevant endpoints that you can call to
  obtain details of a particular building.
deprecated: false
hidden: true
metadata:
  robots: index
---
# <br />API References

This section provides you with the relevant endpoints that you can call to obtain details of a particular building.

## <br />Get Building Details

This endpoint returns information about a specific building.

### Endpoint

**URL**: GET /api/v1/buildings/{buildingId}

### Path Parameters

| Field Name | Data Type | Mandatory | Description                                                                                                                          |
| ---------- | --------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| buildingId | Integer   | Yes       | A Unique  identifier for the building assigned by the system, allowing users to reference and manage specific buildings effectively. |

***

### Example Request

```http
http GET https\:/ /api/v1/buildings/1023\
accept: application/json
```

<br />

***

### Response

```json
<br />

{
  "id":1023,
  "name":"London Headquarters",
  "status":"Online",
  "timezone":"Europe/London",
  "floors":12
}
```

***

### Status Codes

| Code | Description           |
| ---- | --------------------- |
| 200  | Success               |
| 400  | Invalid Request       |
| 401  | Unauthorized          |
| 404  | Building Not Found    |
| 500  | Internal Server Error |

<br />
