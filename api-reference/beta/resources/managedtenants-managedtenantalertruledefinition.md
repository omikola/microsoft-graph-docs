---
title: "managedTenantAlertRuleDefinition resource type"
description: "Represents the alert rule definition used to create alert rules in Microsoft 365 Lighthouse."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantAlertRuleDefinition resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The Microsoft built and designed rule templates will be used by Azure AD users when they create their own alert rules. The rule definitions will be designed by Microsoft, the only editing capability the user has is changing the default settings and suggested alert severity.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenantAlertRuleDefinitions](../api/managedtenants-managedtenant-list-managedtenantalertruledefinitions.md)|[microsoft.graph.managedTenants.managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) collection|Get a list of the [microsoft.graph.managedTenants.managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) objects and their properties.|
|[Get managedTenantAlertRuleDefinition](../api/managedtenants-managedtenantalertruledefinition-get.md)|[microsoft.graph.managedTenants.managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managedTenantAlertRuleDefinition](../resources/managedtenants-managedtenantalertruledefinition.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|`id`|`String`| The unique identifier of the alert rule. Required. Read-only.|
|`createdByUserId`|`String`| The Azure AD user id of the user who created this entity. Ex: "7123ee95-1dc9-4f0b-be17-84962987c9de" Optional. Readonly. |
|`createdDateTime`|`DateTimeOffset`|The date and time at which this entity was created. Optional. Readonly. |
|`lastActionByUserId`|`String`|The Azure AD user id of the user who last modified this entity. Ex: "d82f805d-171c-4989-9c1a-df5016961d13" Optional. Readonly. |
|`lastActionDateTime`|`DateTimeOffset`| The date and time at which this entity was last modified. Optional. Readonly. |
| `definitionTemplate` | `microsoft.graph.managedTenants.alertRuleDefinitionTemplate` | The template used to create the alertRuleDefinition. Optional. Readonly |
| `displayName` | `string` | The display name of the alertRule. Ex: "Risky User Alert Rule Template"  Optional. Readonly |
|`settings`|`Collection(microsoft.graph.managedTenants.managementTemplateStepSetting)`|The default settings used when initially creating a new alert rule. These are the initial, recommended settings. The Azure AD user can change these how they see fit and those new settings are store in the alert rule's applied settings.  Optional. Readonly |
| `referenceStrings` | `Collection(microsoft.graph.managedTenants.ManagementTemplateStepSettingReferenceString) | A collection of string that will be used to reference alert title tokens stored on the definition template. Optional. Readonly. |

#### alertRuleDefinitionTemplate Properties

| Property |Type|Description|
|:---|:---|:---|
| `defaultSeverity` | `microsoft.graph.managedTenants.alertSeverity` | The default severity for the alertRule and the alert itself. The Azure AD user can change the set value on the alert rule during rule creation. This is the Microsoft suggested severity and cannot be changed on the alert rule definition template. The possible values are: `informational`, `low`, `medium`, `high`, `unknownFutureValue`. Optional. Readonly. |

### alertSeverity values

|Member|Description|
|:---|:---|
| `unknown` | Default. Set to unknown if no severity is assigned to the alert. |
| `informational` | Indicates the alert is informational and no immediate action is needed. |
| `low` | Indicates the alert has a low severity and should not be done first compared to a high severity alert. |
| `medium` | Indicates the alert has a medium severity and should take precedence over a low severity or informational alert. |
| `high` | Indicates the alert has a high severity and should be actioned upon sooner than any other non-high severity alert. |
| `unknownFutureValue` | unknownFutureValue for evolvable enums pattern. |

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|`alertRules`|`Collection(microsoft.graph.managedTenants.managedTenantAlertRule)` |The managedTenantAlertRules generated using this managedTenantAlertRuleDefinition.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantAlertRuleDefinition",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantAlertRuleDefinition",
  "id": "String (identifier)",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String",
  "displayName": "String",
  "settings": "Collection(microsoft.graph.managedTenants.managementTemplateStepSetting)"
}
```
