---
title: "managedTenantAlertLog resource type"
description: "Represents a log that can be attached to an alert made in Microsoft 365 Lighthouse."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantAlertLog resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A log attached to a managedTenantAlert the Azure AD user can add. The log can store any information conveyed through plain text. 

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenantAlertLogs](../api/managedtenants-managedtenant-list-managedtenantalertlogs.md)|[microsoft.graph.managedTenants.managedTenantAlertLog](../resources/managedtenants-managedtenantalertlog.md) collection|Get a list of the [microsoft.graph.managedTenants.managedTenantAlertLog](../resources/managedtenants-managedtenantalertlog.md) objects and their properties.|
|[Get managedTenantAlertLog](../api/managedtenants-managedtenantalertlog-get.md)|[microsoft.graph.managedTenants.managedTenantAlertLog](../resources/managedtenants-managedtenantalertlog.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managedTenantAlertLog](../resources/managedtenants-managedtenantalertlog.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|`id`|`String`| The unique identifier of the alert log. Required. Read-only.|
|`content`|`microsoft.graph.managedTenants.alertLogContent`|The content of the log. Anyone adding a log can add plain text to be stored. Ex: "The alert was set off by a password change. The risk has been mitigated." Optional. |
|`createdDateTime`|`DateTimeOffset`| The date and time at which this entity was created. Optional. Read-only.|
|`createdByUserId`|`String`|  The Azure AD user id of the user who created this entity. Ex: "7123ee95-1dc9-4f0b-be17-84962987c9de" Optional. Read-only. |
|`lastActionByUserId`|`String`| The Azure AD user id of the user who last modified this entity. Ex: "d82f805d-171c-4989-9c1a-df5016961d13". Optional. Read-only.|
|`lastActionDateTime`|`DateTimeOffset`| The date and time at which this entity was last modified. Optional. Read-only.|

### alertLogContent Properties

| Property | Type | Description |
|:---|:---|:---|
| `displayName` | `String` | The display name for the alertLogContent. Ex: "Plain text log" Optional. |

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|`alert`|`managedTenantAlert`|The alert the log is attached to.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlertLog",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantAlertLog",
  "id": "String (identifier)",
  "content": "microsoft.graph.managedTenants.alertLogContent",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String"
}
```
