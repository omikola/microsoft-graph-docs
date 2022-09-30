---
title: "List managedTenantEmailNotifications"
description: "Get a list of the managedTenantEmailNotifications objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantEmailNotifications
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantEmailNotifications](../resources/managedtenants-managedtenantemailnotification.md) objects and their properties.

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
GET /tenantRelationships/managedTenants/managedTenantEmailNotifications
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

If successful, this method returns a `200 OK` response code and a collection of [managedTenantEmailNotifications](../resources/managedtenants-managedtenantemailnotification.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantEmailNotifications
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantEmailNotifications)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantEmailNotifications",
    "value": [
        {
            "id": "7a80d6a8-9a00-4b58-b691-684d9316d5f3",
            "subject": "Risky User Detected",
            "emailBody": "A risky user was detected for a tenant.",
            "emailAddresses": [
              {
                "emailAddress": "connie@contoso.com"
              },
              {
                "emailAddress": "ron@contoso.com"
              }
            ],
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
        },
        {
            "id": "03fa206e-d2cb-4ec8-9e2f-8b667a50578b",
            "subject": "MFA Not Enabled For User",
            "emailBody": "Some users do not have MFA enabled.",
            "emailAddresses": [
              {
                "emailAddress": "johnsmith@contoso.com"
              },
              {
                "emailAddress": "joy@contoso.com"
              }
            ],
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
        }
    ]
}
```
