---
title: "List managedTenantTicketingEndpoints"
description: "Get a list of the managedTenantTicketingEndpoints objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantTicketingEndpoints
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantTicketingEndpoints](../resources/managedtenants-managedtenantticketingendpoint.md) objects and their properties.

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
GET /tenantRelationships/managedTenants/managedTenantTicketingEndpoints
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

If successful, this method returns a `200 OK` response code and a collection of [managedTenantTicketingEndpoints](../resources/managedtenants-managedtenantticketingendpoint.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantTicketingEndpoints
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantTicketingEndpoints)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantTicketingEndpoints",
    "value": [
        {
            "id": "b695af4a-76fe-48a6-9181-48b16db88ec2",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
            "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
            "displayName": "Connect Wise",
            "email": "ContosoTickets@ConnectWise.com",
            "phone": "2115554098"
        },
        {
            "id": "a680d4c1-6170-4ca9-87ee-68edc231cf18",
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000",
            "displayName": "Datto",
            "email": "ContosoTickets@Datto.com",
            "phone": "7815553719"
        }
    ]
}
```
