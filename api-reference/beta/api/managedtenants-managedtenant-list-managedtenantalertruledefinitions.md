---
title: "List managedTenantAlertRuleDefinitions"
description: "Get a list of the managedTenantAlertRuleDefinitions objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantAlertRuleDefinitions
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) objects and their properties.

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

If successful, this method returns a `200 OK` response code and a collection of [managedTenantAlertRuleDefinitions](../resources/managedtenants-managedtenantalertruledefinition.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlertRuleDefinitions
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantAlertRuleDefinitions)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlertRuleDefinitions",
    "value": [
        {
            "id": "63cad036-19f4-41d7-a423-ccfdcdcadd30",
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
            },
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
        },
        {
            "id": "3c5fa08d-6141-4a31-9047-ea520792e073",
            "displayName": "MFA Not Enabled Template",
            "settings": [
            ],
            "definitionTemplate": {
                "defaultSeverity": "informational"
            },
            "createdDateTime": "2022-08-02T17:42:33.1624374Z",
            "createdByUserId": "00000000-0000-0000-0000-000000000000",
            "lastActionDateTime": "2022-08-02T17:42:33.1624374Z",
            "lastActionByUserId": "00000000-0000-0000-0000-000000000000"
        }
    ]
}
```
