---
title: "Get managementTemplateStepTenantSummary"
description: "Read the properties and relationships of a managementTemplateStepTenantSummary object."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# Get managementTemplateStepTenantSummary
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) object.

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
GET /tenantRelationships/managedTenants/managementTemplateStepTenantSummaries/{managementTemplateStepTenantSummaryId}
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

If successful, this method returns a `200 OK` response code and a [managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) object in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementTemplateStepTenantSummaries/{managementTemplateStepTenantSummaryId}
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managementTemplateStepTenantSummary"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

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
```
