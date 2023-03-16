---
title: "managementTemplateCollectionTenantSummary resource type"
description: "Represents the summary of a managementTemplateCollection on a tenant."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managementTemplateCollectionTenantSummary resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the summary of a [managementTemplateCollection](../resources/managedtenants-managementtemplatecollection.md) on a tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managementTemplateCollectionTenantSummaries](../api/managedtenants-managedtenant-list-managementtemplatecollectiontenantsummaries.md)|[microsoft.graph.managedTenants.managementtemplatecollectiontenantsummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) collection|Get a list of the [microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) objects and their properties.|
|[Get managementTemplateCollectionTenantSummary](../api/managedtenants-managementtemplatecollectiontenantsummary-get.md)|[microsoft.graph.managedTenants.managementtemplatecollectiontenantsummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) object.|

## Properties
| Property                                | Type           | Description                                                                                                                                                           |
|:----------------------------------------|:---------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id                                      | String         | The unique identifier for the entity. Required. Read-only.                                                                                                            |
| createdDateTime                         | DateTimeOffset | The date and time when this entity was created. Required. Read-only.                                                                                                  |
| createdByUserId                         | String         | The unique identifier for the Azure Active Directory (Azure AD) user who created this entity. Required. Read-only.                                                    |
| lastActionDateTime                      | DateTimeOffset | The date and time when this entity was last modified. Normally caused by activities in the related **managementTemplateCollections**. Read-only.                      |
| lastActionByUserId                      | String         | The unique identifier for the Azure AD user who last modified this entity. Normally caused by activities in the related **managementTemplateCollections**. Read-only. |
| tenantId                                | String         | The tenant ID associated with this summary. Required. Read-only.                                                                                                      |
| managementTemplateCollectionId          | String         | The unique identifier for the **managementTemplateCollection** associated with this summary. Required. Read-only.                                                     |
| managementTemplateCollectionDisplayName | String         | The **managementTemplateCollection** display name associated with this summary.  Required. Read-only.                                                                 |
| isComplete                              | Boolean        | Indicates whether this **tenantId**, **managementTemplateCollectionId** pair is complete. Required. Read-only.                                                        |
| completeStepsCount                      | Int32          | The number of complete steps associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                         |
| incompleteStepsCount                    | Int32          | The number of incomplete steps associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| dismissedStepsCount                     | Int32          | The number of dismissed steps associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                        |
| ineligibleStepsCount                    | Int32          | The number of ineligible steps associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| regressedStepsCount                    | Int32          | The number of regressed steps associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| unlicensedUsersCount                    | Int32          | The number of unlicensed users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| regressedUsersCount                    | Int32          | The number of regressed users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| completeUsersCount                      | Int32          | The number of complete users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                         |
| incompleteUsersCount                    | Int32          | The number of incomplete users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                       |
| excludedUsersCount                      | Int32          | The number of excluded users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                         |
| excludedUsersDistinctCount              | Int32          | The number of distinct excluded users associated with this **tenantId**, **managementTemplateCollectionId** pair. Required. Read-only.                                |

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary",
  "completeStepsCount": "Int32",
  "completeUsersCount": "Int32",
  "createdByUserId": "String",
  "createdDateTime": "DateTimeOffset",
  "dismissedStepsCount": "Int32",
  "excludedUsersCount": "Int32",
  "id": "String (identifier)",
  "regressedStepsCount": "Int32",
  "unlicensedUsersCount": "Int32",
  "regressedStepsCount": "Int32",			
  "regressedUsersCount": "Int32",
  "incompleteUsersCount": "Int32",
  "ineligibleStepsCount": "Int32",
  "isComplete": "Boolean",
  "lastActionByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "managementTemplateCollectionDisplayName": "String",
  "managementTemplateCollectionId": "String",
  "tenantId": "String"
}
```
