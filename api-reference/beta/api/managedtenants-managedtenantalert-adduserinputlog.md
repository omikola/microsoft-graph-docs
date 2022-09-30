---
title: "managedTenantAlert: addUserInputLog"
description: "Adds a log from the user to an alert."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# tenantTag: assignTag
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

An action to add a plain text log to an alert. Azure AD users can add plain text content to be logged on the alert. Note that this action is bounded to managedTenantAlerts and not managedTenantAlertLogs.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ManagedTenants.WriteRead.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /tenantRelationships/managedTenants/managedTenantAlerts/{managedTenantAlertId}/addUserInputLog
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Parameter|Type|Description|
|:---|:---|:---|
| `logInformation` | `String` | The content to be put into the log. This plain text will be stored in a log attached to an alert. Ex: "The alert was set off by a password change. The risk has been mitigated." |

## Response

If successful, this action returns a `200 OK` response code and a [managedTenantAlert](../resources/managedtenants-managedtenantalert.md) in the response body.

## Examples

### Request

``` http
POST https://graph.microsoft.com/beta/tenantRelationships/managedTenantAlerts/tenantTags/{managedTenantAlertId}/addUserInputLog
Content-Type: application/json

{
  "logInformation": "User reset their password."
}
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlert"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#managedTenantAlerts/$entity",
  id": "59921056-05cc-4c54-a63e-f3aaad7907a1",
  "id": "b695af4a-76fe-48a6-9181-48b16db88ec2",
  "title": "Risky User Detected",
  "message": "A risky user in the following tenant was detected.",
  "correlationId": "a7fc9ec3-16a4-4b9f-b454-1902cf8ec933",
  "correlationCount": 0,
  "tenantId": "cc7c2651-148e-41c4-987a-80ed400b0681",
  "assignedToUserId": "ad375967-c71d-4e7e-8edc-02c688163616",
  "status": "newAlert",
  "severity": "high",
  "alertLogs": [
    {
      "content": "User reset their password."
    }
  ]
  "createdDateTime": "2022-08-02T17:42:33.1624374Z",
  "createdByUserId": "00000000-0000-0000-0000-000000000000",
  "lastActionDateTime": "2022-08-03T12:31:56.1923426Z",
  "lastActionByUserId": "ad375967-c71d-4e7e-8edc-02c688163616"
}
```
