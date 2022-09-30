---
title: "Get managedTenantAlert"
description: "Read the properties and relationships of a managedTenantAlert object."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# Get managedTenantAlert
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [managedTenantAlert](../resources/managedtenants-managedtenantalert.md) object.

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
GET /tenantRelationships/managedTenants/managedTenantAlerts/{managedTenantAlertId}
```

## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response, including `$apply`, `$count`, `$expand`, `$filter`, `$orderBy`, `$select`, `$skip`, and `$top`.

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [managedTenantAlert](../resources/managedtenants-managedtenantalert.md) object in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlerts/{managedTenantAlertId}
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlert"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlerts/$entity",
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
}
```
