---
title: "Get managedTenantAlertRuleDefinition"
description: "Read the properties and relationships of a managedTenantAlertRuleDefinition object."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# Get managedTenantAlertRuleDefinition
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) object.

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
GET /tenantRelationships/managedTenants/managedTenantAlertRuleDefinitions/{managedTenantAlertRuleDefinitionId}
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

If successful, this method returns a `200 OK` response code and a [managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) object in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlertRuleDefinitions/{managedTenantAlertRuleDefinitionId}
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlertRuleDefinition"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlertRuleDefinitions/$entity",
  "id": "62722027-3148-4ff7-a8b0-0b048ab6e19f",
  "createdDateTime": "2022-09-23T17:42:33.1624374Z",
  "createdByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de",
  "lastActionDateTime": "2022-09-23T17:42:33.1624374Z",
  "lastActionByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de",
  "displayName": "Risky User Template",
  "settings": [
      {
          "displayName": "Risk State",
          "valueType": "StringCollection",
          "value": "[\"atRisk\"]"
      }
  ],
  "definitionTemplate": {
      "defaultSeverity": "high"
  }
}
```
