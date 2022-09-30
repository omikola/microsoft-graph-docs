---
title: "managedTenantEmailNotification resource type"
description: "Represents the email notification to notify users about alerts in Microsoft 365 Lighthouse."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantEmailNotification resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The notification sent to an Azure AD user via the UX/API when an alert is created. UX alerts will appear similar to a pop up. The user can also query the database for notifications.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenantEmailNotifications](../api/managedtenants-managedtenant-list-managedtenantemailnotifications.md)|[microsoft.graph.managedTenants.managedTenantEmailNotification](../resources/managedtenants-managedtenantemailnotification.md) collection|Get a list of the [microsoft.graph.managedTenants.managedTenantEmailNotification](../resources/managedtenants-managedtenantemailnotification.md) objects and their properties.|
|[Get managedTenantEmailNotification](../api/managedtenants-managedtenantemailnotification-get.md)|[microsoft.graph.managedTenants.managedTenantEmailNotification](../resources/managedtenants-managedtenantemailnotification.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managedTenantEmailNotification](../resources/managedtenants-managedtenantemailnotification.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|`id`|`String`| The unique identifier of the notification. Required. Read-only.|
|`createdByUserId`|`String`| The Azure AD user id of the user who created this entity. Ex: "7123ee95-1dc9-4f0b-be17-84962987c9de" Optional. Readonly. |
|`createdDateTime`|`DateTimeOffset`|The date and time at which this entity was created. Optional. Readonly. |
|`lastActionByUserId`|`String`|The Azure AD user id of the user who last modified this entity. Ex: "d82f805d-171c-4989-9c1a-df5016961d13" Optional. Readonly. |
|`lastActionDateTime`|`DateTimeOffset`| The date and time at which this entity was last modified. Optional. Readonly. |
|`emailAddresses`|`Collection(microsoft.graph.managedTenants.email)`|A list of email addresses the notification will be sent to. The email addresses are the emails of the Azure AD users. Optional. Readonly. |
|`emailBody`|`String`|The message contained in the email notification. Ex: "A risky user in Contoso was detected." Optional. Readonly. |
|`subject`|`String`|The subject of the email notification. Ex: "Risky User Detected". Optional. Readonly. |

## email Properties
|Property|Type|Description|
|:---|:---|:---|
| `emailAddress` | `String` | The address to send emails to. Ex: "ConnectWiseTickets@contoso.com". Optional. Readonly. |

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|`alert`|`managedTenantAlert`|The alert that caused the notification to be generated.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantEmailNotification",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantEmailNotification",
  "id": "String (identifier)",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String",
  "emailAddresses": "Collection(microsoft.graph.managedTenants.email)",
  "emailBody": "String",
  "subject": "String"
}
```
