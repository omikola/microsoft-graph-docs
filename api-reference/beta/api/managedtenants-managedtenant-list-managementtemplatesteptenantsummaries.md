---
title: "List managementTemplateStepTenantSummaries"
description: "Get a list of the managementTemplateStepTenantSummary objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managementTemplateStepTenantSummaries
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) objects and their properties.

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
GET /tenantRelationships/managedTenants/managementTemplateStepTenantSummaries
```

## Optional query parameters
This method supports the `$apply`, `$count`, `$expand`, `$filter`, `$orderBy`, `$select`, and `$top` [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [managementTemplateStepTenantSummaries](../resources/managedtenants-managementtemplatesteptenantsummary.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementTemplateStepTenantSummaries
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managementTemplateStepTenantSummaries)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/tenantRelationships/managedTenants/$metadata#managementTemplateStepTenantSummary",
    "value": [
        {
            "@odata.etag": "\"5600b9b4-0000-0800-0000-61d51be10000\"",
            "managementTemplateCollectionId": "1c13b9c3-1f65-4472-81a8-da6c8c95cbf4",
            "managementTemplateCollectionDisplayName": "collection",
            "managementTemplateId": "2c13b9c3-1f65-4472-81a8-da6c8c95cbf4",
            "managementTemplateDisplayName": "template",
            "managementTemplateStepId": "3c13b9c3-1f65-4472-81a8-da6c8c95cbf4",
            "managementTemplateStepDisplayName": "step",
            "assignedTenantsCount": 304,
            "compliantTenantsCount": 11,
            "notCompliantTenantsCount": 234,
            "dismissedTenantsCount": 4,
            "ineligibleTenantsCount": 55
        }
    ]
}
```
