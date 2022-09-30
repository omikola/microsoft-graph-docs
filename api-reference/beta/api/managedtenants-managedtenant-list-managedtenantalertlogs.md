---
title: "List managedTenantAlertLogs"
description: "Get a list of the managedTenantAlertLogs objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantAlertLogs
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantAlertLogs](../resources/managedtenants-managedtenantalertlog.md) objects and their properties.

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
GET /tenantRelationships/managedTenants/managedTenantAlertLogs
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

If successful, this method returns a `200 OK` response code and a collection of [managedTenantAlertLogs](../resources/managedtenants-managedtenantalertlog.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlertLogs
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantAlertLogs)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlertLogs",
    "value": [
        {
            "id": "b695af4a-76fe-48a6-9181-48b16db88ec2",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
            "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
            "content": "Alert was triggered because a user does not have MFA set up."
        },
        {
            "id": "aff82a54-dc18-44a8-93fe-6b81a958b9a4",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
            "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
            "content": "Alert status changed from inProgress to Closed."
        },
        {
            "id": "7c6cec66-8843-402f-a5c2-0ccba2a62c5f",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
            "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
            "content": "User decided to reset their password."
        }
    ]
}
```
