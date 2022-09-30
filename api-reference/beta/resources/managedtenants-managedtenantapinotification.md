---
title: "managedTenantApiNotification resource type"
description: "Represents the api/ux notification to notify users about alerts in Microsoft 365 Lighthouse."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantApiNotification resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The notification sent to an Azure AD user via the UX/API when an alert is created. UX alerts will appear similar to a pop up. The user can also query the database for notifications.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenantApiNotifications](../api/managedtenants-managedtenant-list-managedtenantapinotifications.md)|[microsoft.graph.managedTenants.managedTenantApiNotification](../resources/managedtenants-managedtenantapinotification.md) collection|Get a list of the [microsoft.graph.managedTenants.managedTenantApiNotification](../resources/managedtenants-managedtenantapinotification.md) objects and their properties.|
|[Get managedTenantApiNotification](../api/managedtenants-managedtenantapinotification-get.md)|[microsoft.graph.managedTenants.managedTenantApiNotification](../resources/managedtenants-managedtenantapinotification.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managedTenantApiNotification](../resources/managedtenants-managedtenantapinotification.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|`id`|`String`| The unique identifier of the notification. Required. Read-only.|
|`createdByUserId`|`String`| The Azure AD user id of the user who created this entity. Ex: "7123ee95-1dc9-4f0b-be17-84962987c9de" Optional. Readonly. |
|`createdDateTime`|`DateTimeOffset`|The date and time at which this entity was created. Optional. Readonly. |
|`lastActionByUserId`|`String`|The Azure AD user id of the user who last modified this entity. Ex: "d82f805d-171c-4989-9c1a-df5016961d13" Optional. Readonly. |
|`lastActionDateTime`|`DateTimeOffset`| The date and time at which this entity was last modified. Optional. Readonly. |
|`userId`|`String`|The Id of the Azure AD user the notification will be sent to. Ex: "639d837d-cf46-427e-9ddc-3a5630b698cf". Optional. Read-only.|
|`message`|`String`|The message contained in the notification. Ex: "A risky user from Contoso was detected". Optional. Read-only.|
|`title`|`String`|The title of the notification. Ex: "Risky User Detected". Optional. Read-only.|
|`isAcknowledged`|`Boolean`| An indication of whether the Azure AD user has acknowledged the alert. When false, the user has not acknowledged the notification. When true, the user has acknowledged the notification and the alert. The default is false. Optional. Read-only.|


## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|`alert`|`managedTenantAlert`|The alert that caused the notification to be generated.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantApiNotification",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantApiNotification",
  "id": "String (identifier)",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String",
  "userId": "String",
  "message": "String",
  "title": "String",
  "isAcknowledged": "Boolean"
}
```
