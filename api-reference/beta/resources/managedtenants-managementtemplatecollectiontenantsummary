---
title: "managementTemplateCollectionTenantSummary resource type"
description: "A summary of a managementTemplateCollection on a tenant."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantAlert resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A summary of a managementTemplateCollection on a tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managementTemplateCollectionTenantSummaries](../api/managedtenants-managedtenant-list-managementtemplatecollectiontenantsummaries.md)|[microsoft.graph.managedTenants.managementtemplatecollectiontenantsummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) collection|Get a list of the [microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) objects and their properties.|
|[Get managementTemplateCollectionTenantSummary](../api/managedtenants-managementtemplatecollectiontenantsummary-get.md)|[microsoft.graph.managedTenants.managementtemplatecollectiontenantsummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managementTemplateCollectionTenantSummary](../resources/managedtenants-managementtemplatecollectiontenantsummary.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
| `id`            | `Edm.String` | The unique identifier of entity. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `createdDateTime`                  | `Edm.DateTimeOffset`                                    | The date and time at which this entity was created. Required. Read-only.  | Yes  | Yes      | Yes      |
| `createdByUserId`                  | `Edm.String`                                    | The Azure AD user id of the user who created this entity. Required. Read-only.  | Yes  | Yes      | Yes      |
| `lastActionDateTime`                  | `Edm.DateTimeOffset`                                    | The date and time at which this entity was last modified. Normally caused by activities in the related ManagementTemplateCollections. Read-only.  | Yes  | No      | Yes      |
| `lastActionByUserId`                  | `Edm.String`                                    | The Azure AD user id of the user who last modified this entity. Normally caused by activities in the related ManagementTemplateCollections. Read-only.  | Yes  | No      | Yes      |
| `tenantId`            | `Edm.String` | The tenantId associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateCollectionId`            | `Edm.String` | The managementTemplateCollectionId associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateCollectionDisplayName`            | `Edm.String` | The managementTemplateCollection display name associated with this summary.  Required. Read-only.                                          | Yes | Yes      | Yes      |
| `isComplete`   | `Edm.Boolean` | Indicates whether this tenantId, managementTemplateCollectionId pair is complete. Required. Read-only. | No | Yes      | Yes      |
| `completeStepsCount`   | `Edm.Int32` | The number of complete steps associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `incompleteStepsCount`   | `Edm.Int32` | The number of incomplete steps associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `dismissedStepsCount`   | `Edm.Int32` | The number of dismissed steps associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `ineligibleStepsCount`   | `Edm.Int32` | The number of ineligible steps associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `completeUsersCount`   | `Edm.Int32` | The number of complete users associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `incompleteUsersCount`   | `Edm.Int32` | The number of incomplete users associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `excludedUsersCount`   | `Edm.Int32` | The number of excluded users associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |
| `excludedUsersDistinctCount`   | `Edm.Int32` | The number of distinct excluded users associated with this tenantId, managementTemplateCollectionId pair. Required. Read-only. | No | Yes      | Yes      |

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
  "id": "String (identifier)",
  "tenantId": "String",
  "managementTemplateCollectionId": "String",
  "managementTemplateCollectionDisplayName": "String"
  "isComplete": "Boolean",
  "completeStepsCount": "Int32",
  "incompleteStepsCount": "Int32",
  "dismissedStepsCount": "Int32",
  "ineligibleStepsCount": "Int32",
  "completeUsersCount": "Int32",
  "incompleteUsersCount": "Int32",
  "excludedUsersCount": "Int32"
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String"
}
```
