---
title: "List managedTenantAlerts"
description: "Get a list of the managedTenantAlerts objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantAlerts
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantAlerts](../resources/managedtenants-managedtenantalert.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ManagedTenants.Read.All, ManagedTenants.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /tenantRelationships/managedTenants/managedTenantAlerts
```

## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response, including `$apply`, `$count`, `$expand`, `$filter`, `$orderBy`, `$select`, and `$top`.

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [managedTenantAlerts](../resources/managedtenants-managedtenantalert.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlerts
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantAlerts)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlerts",
    "value": [
        {
            "id": "b695af4a-76fe-48a6-9181-48b16db88ec2",
            "title": "Risky User Detected",
            "message": "A risky user in the following tenant was detected.",
            "correlationId": "a7fc9ec3-16a4-4b9f-b454-1902cf8ec933",
            "correlationCount": 0,
            "tenantId": "cc7c2651-148e-41c4-987a-80ed400b0681",
            "assignedToUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
            "status": "newAlert",
            "severity": "high",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
            "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616"
        },
        {
            "id": "a680d4c1-6170-4ca9-87ee-68edc231cf18",
            "title": "Device No Longer Compliant",
            "message": "A device belonging to the following tenant fell out of compliance.",
            "correlationId": "1b5c375f-4547-4dc2-9d24-f8e9b1476427",
            "correlationCount": 0,
            "tenantId": "58458f37-c462-482e-9303-783aeeec7c70",
            "assignedToUserId": null,
            "status": "newAlert",
            "severity": "medium",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
        },
        {
            "id": "59921056-05cc-4c54-a63e-f3aaad7907a1",
            "title": "MFA not enabled",
            "message": "A user for the following tenant does not have MFA enabled.",
            "correlationId": "39fdcc5a-3d01-4e21-bc6b-3b5bf966d9e1",
            "correlationCount": 0,
            "tenantId": "51b22007-f5d6-4e86-8022-cab90d81ddc0",
            "assignedToUserId": "701e622a-8760-4b8a-891f-37a20c68d3cb",
            "status": "inProgress",
            "severity": "informational",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-10T08:51:28.9372810Z",
            "lastActionByUserId": "701e622a-8760-4b8a-891f-37a20c68d3cb"
        }
    ]
}
```
