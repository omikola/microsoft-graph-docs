---
title: "List managedTenantAlertRules"
description: "Get a list of the managedTenantAlertRules objects and their properties."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# List managedTenantAlertRules
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [managedTenantAlertRules](../resources/managedtenants-managedtenantalertrule.md) objects and their properties.

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

If successful, this method returns a `200 OK` response code and a collection of [managedTenantAlertRules](../resources/managedtenants-managedtenantalertrule.md) objects in the response body.

## Examples

### Request

``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managedTenantAlertRules
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.managedTenantAlertRules)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/managedTenants/managedTenantAlertRules",
    "value": [
        {
            "id": "62722027-3148-4ff7-a8b0-0b048ab6e19f",
            "tenantIds": [
                "3b646157-f0ec-4aad-b054-5c0149b73ffa",
                "5f9ab713-6346-476d-8e77-f05922223670"
            ],
            "appliedSettings": [
                {
                    "displayName": "Risk State",
                    "valueType": "StringCollection",
                    "value": "[\"atRisk\"]"
                }
            ],
            "alertDisplayName": "Risky User Detected",
            "severity": "high",
            "notificationFinalDestinations": "api",
            "alertRuleDisplayName": "Risky User Rule",
            "alertRuleDescription": "Rule used to detect risky users.",
            "createdDateTime": "2022-09-23T17:42:33.1624374Z",
            "createdByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de",
            "lastActionDateTime": "2022-09-23T17:42:33.1624374Z",
            "lastActionByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de"
        },
        {
            "id": "44e9ee04-b49c-4c02-874d-f07d78ec5125",
            "tenantIds": [
                "3c5fa08d-6141-4a31-9047-ea520792e073"
            ],
            "appliedSettings": [
                {
                    "displayName": "Risk State",
                    "valueType": "StringCollection",
                    "value": "[\"atRisk\"]"
                }
            ],
            "alertDisplayName": "Risky User Detected",
            "severity": "medium",
            "notificationFinalDestinations": "api,email",
            "alertRuleDisplayName": "Risky User Rule For Contoso",
            "alertRuleDescription": "Rule used to detect risky users for Contoso.",
            "createdDateTime": "2022-09-23T17:42:33.1624374Z",
            "createdByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de",
            "lastActionDateTime": "2022-09-23T17:42:33.1624374Z",
            "lastActionByUserId": "c7803230-0181-43fd-84ea-9d0f208d72de"
        }
    ]
}
```
