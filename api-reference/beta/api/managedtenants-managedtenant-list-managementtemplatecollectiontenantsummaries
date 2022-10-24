---
title: "List managementTemplateCollectionTenantSummaries"
description: "Get a list of the managementTemplateCollectionTenantSummaries objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantAlerts
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managementTemplateCollectionTenantSummaries](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) objects and their properties.

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
GET /tenantRelationships/managedTenants/managementTemplateCollectionTenantSummaries
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

If successful, this method returns a `200 OK` response code and a collection of [managementTemplateCollectionTenantSummaries](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementTemplateCollectionTenantSummaries
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managementTemplateCollectionTenantSummaries)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json
{
    "@odata.context": "https://graph.microsoft.com/beta/tenantRelationships/managedTenants/$metadata#managementTemplateCollectionTenantSummary",
    "value": [
        {
            "@odata.etag": "\"5600b9b4-0000-0800-0000-61d51be10000\"",
			"tenantId": "b0228dfe-93da-42dc-924a-3735fb8204b2",
			"managementTemplateCollectionId": "1c13b9c3-1f65-4472-81a8-da6c8c95cbf4",
            "isComplete": false,
			"completeStepsCount": 2,
			"incompleteStepsCount": 2,
			"dismissedStepsCount": 2,
			"ineligibleStepsCount": 1,
			"completeUsersCount": 40,
			"incompleteUsersCount": 32,
			"excludedUsersCount": 21
        }
    ]
}
```
