---
title: "Get managedTenantApiNotification"
description: "Read the properties and relationships of a managedTenantApiNotification object."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# Get managedTenantApiNotification
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [managedTenantApiNotification](../resources/managedtenants-managedtenantalertapinotification.md) object.

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
GET /tenantRelationships/managedTenants/managedTenantApiNotifications/{managedTenantApiNotificationId}
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

If successful, this method returns a `200 OK` response code and a [managedTenantApiNotification](../resources/managedtenants-managedtenantalertapinotification.md) object in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantApiNotifications/{managedTenantApiNotificationId}
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managedTenantApiNotification"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantApiNotifications/$entity",
  "id": "7a80d6a8-9a00-4b58-b691-684d9316d5f3",
  "title": "Risky User Detected",
  "message": "A risky user was detected for a tenant.",
  "userId": "6d91dedc-25ed-4828-8942-2c8b8a6c8090",
  "acknowledged": false,
  "createdDateTime": "2022-08-02T17:42:33.1624374Z",
  "createdByUserId": "00000000-0000-0000-0000-000000000000",
  "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
  "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
}
```
