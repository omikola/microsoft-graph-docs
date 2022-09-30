---
title: "managedTenantAlertRule resource type"
description: "Represents the alert rule used to generated alerts in Microsoft 365 Lighthouse."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantAlertRule resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A set of conditions that, when met, create a managedTenantAlert. The Azure AD user can edit those conditions as they see fit. When notificationDestinations and targets are set, the specified targets will be alerted upon the creation of the alerts.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenantAlertRules](../api/managedtenants-managedtenant-list-managedtenantalertrules.md)|[microsoft.graph.managedTenants.managedTenantAlertRule](../resources/managedtenants-managedtenantalertrule.md) collection|Get a list of the [microsoft.graph.managedTenants.managedTenantAlertRule](../resources/managedtenants-managedtenantalertrule.md) objects and their properties.|
|[Get managedTenantAlertRule](../api/managedtenants-managedtenantalertrule-get.md)|[microsoft.graph.managedTenants.managedTenantAlertRule](../resources/managedtenants-managedtenantalertrule.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managedTenantAlertRule](../resources/managedtenants-managedtenantalertrule.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|`id`|`String`| The unique identifier of the alert rule. Required. Read-only.|
|`displayName`|`String`| The name of the managedTenantAlertRule. Ex: "Detect Risky Users in Gold Star Customers". Optional. |
|`description`|`String`| The description of the managedTenantAlertRule. Ex: "This rule creates alerts for only the Gold Star customers. Risky users by non-Gold Star customers will not be alerted on." Optional. |
|`alertDisplayName`|`String`| The title of a generated alert. Ex: "Gold Star Risky User Detected". Optional. |
|`appliedSettings`|`Collection(microsoft.graph.managedTenants.managementTemplateStepSetting)`|The settings the defined when the rule is created. These are the settings that will be used when running the rules. Ex: You may want to only detect "High risk" risky users instead of detecting users with any risk, low or high. Optional. |
|`createdByUserId`|`String`| The Azure AD user id of the user who created this entity. Ex: "7123ee95-1dc9-4f0b-be17-84962987c9de" Optional. Readonly. |
|`createdDateTime`|`DateTimeOffset`|The date and time at which this entity was created. Optional. Readonly. |
|`lastActionByUserId`|`String`|The Azure AD user id of the user who last modified this entity. Ex: "d82f805d-171c-4989-9c1a-df5016961d13" Optional. Readonly. |
|`lastActionDateTime`|`DateTimeOffset`| The date and time at which this entity was last modified. Optional. Readonly. |
|`lastRunDateTime`|`DateTimeOffset`|The date and time at which the rule was last run. Optional. Readonly. |
|`notificationFinalDestinations`|`microsoft.graph.managedTenants.notificationDestination`|A set of ways the notification can be sent.The possible values are: `none`, `api`, `email`, `sms`, `unknownFutureValue`. Default is `none`.  Optional. |
|`severity`|`alertSeverity`|The severity to set the alert to.The possible values are: `informational`, `low`, `medium`, `high`, `unknownFutureValue`. Default is `informational`. Optional. |
|`targets`|`Collection(microsoft.graph.managedTenants.notificationTarget)`|Which Azure AD users, security groups, user groups, etc. to send the notifications to. Optional. |
|`tenantIds`|`Collection(microsoft.graph.managedTenants.tenantInfo)`|The Azure AD tenants to run the alert rule on. Contains the Azure AD tenant Id. Optional. |
|`alertTTL`|`int`| The time for the alert to live in the database after creation in seconds.  Optional. Readonly. |

### notificationTarget Properties

|Property|Type|Description|
|:---|:---|:---|
| `displayName` | `String` | The display name for the notificationTarget. Ex: "Security group notification target" Optional. |

### alertSeverity values

|Member|Description|
|:---|:---|
| `unknown` | Default. Set to unknown if no severity is assigned to the alert. |
| `informational` | Indicates the alert is informational and no immediate action is needed. |
| `low` | Indicates the alert has a low severity and should not be done first compared to a high severity alert. |
| `medium` | Indicates the alert has a medium severity and should take precedence over a low severity or informational alert. |
| `high` | Indicates the alert has a high severity and should be actioned upon sooner than any other non-high severity alert. |
| `unknownFutureValue` | unknownFutureValue for evolvable enums pattern. |

### notificationDestination (flag) values

|Member|Description|
|:---|:---|
| `none` | Default. When set to none, no notifications will be sent when the alert is generated. |
| `api` | Indicates that the notification will be sent through the api. |
| `email` | Indicates that the notification will be sent through an email. |
| `sms` | Indicates that the notification will be sent through an sms message. |
| `unknownFutureValue` | unknownFutureValue for evolvable enums pattern. |

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|`alerts`|`Collection(microsoft.graph.managedTenants.managedTenantAlert)`|The alerts generated when the rule is run.|
|`ruleDefinition`|`managedTenantAlertRuleDefinition`|The default definition/template for the rule. Contains default settings that can be changed upon rule creation.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlertRule",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantAlertRule",
  "id": "String (identifier)",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String",
  "tenantIds": "Collection(String)",
  "appliedSettings": "Collection(microsoft.graph.managedTenants.managementTemplateStepSetting)",
  "alertDisplayName": "String",
  "severity": "alertSeverity",
  "notificationFinalDestinations": "notificationDestination",
  "alertRuleDisplayName": "String",
  "alertRuleDescription": "String"
}
```
