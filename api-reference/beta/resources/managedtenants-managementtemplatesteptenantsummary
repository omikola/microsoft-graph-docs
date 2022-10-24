---
title: "managementTemplateStepTenantSummary resource type"
description: "A summary of a managementTemplateStep on a tenant."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managedTenantAlert resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A summary of a managementTemplateStep on a tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managementTemplateStepTenantSummaries](../api/managedtenants-managedtenant-list-managementtemplatesteptenantsummaries.md)|[microsoft.graph.managedTenants.managementtemplatesteptenantsummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) collection|Get a list of the [microsoft.graph.managedTenants.managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) objects and their properties.|
|[Get managementTemplateStepTenantSummary](../api/managedtenants-managementtemplatesteptenantsummary-get.md)|[microsoft.graph.managedTenants.managementtemplatesteptenantsummary](../resources/managedtenants-managementtemplatesteptenantsummary.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
| `id`            | `Edm.String` | The unique identifier of entity. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `createdDateTime`                  | `Edm.DateTimeOffset`                                    | The date and time at which this entity was created. Required. Read-only.  | Yes  | Yes      | Yes      |
| `createdByUserId`                  | `Edm.String`                                    | The Azure AD user id of the user who created this entity. Required. Read-only.  | Yes  | Yes      | Yes      |
| `lastActionDateTime`                  | `Edm.DateTimeOffset`                                    | The date and time at which this entity was last modified. Normally caused by activities in the related ManagementTemplateCollections. Read-only.  | Yes  | No      | Yes      |
| `lastActionByUserId`                  | `Edm.String`                                    | The Azure AD user id of the user who last modified this entity. Normally caused by activities in the related ManagementTemplateCollections. Read-only.  | Yes  | No      | Yes      |
| `managementTemplateCollectionId`            | `Edm.String` | The managementTemplateCollectionId associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateCollectionDisplayName`            | `Edm.String` | The managementTemplateCollection display name associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateId`            | `Edm.String` | The managementTemplateId associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateDisplayName`            | `Edm.String` | The managementTemplate display name associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateStepId`            | `Edm.String` | The managementTemplateStepId associated with this summary. Required. Read-only.                                           | Yes | Yes      | Yes      |
| `managementTemplateDisplayName`            | `Edm.String` | The managementTemplateStep display name associated with this summary.  Required. Read-only.                                          | Yes | Yes      | Yes      |
| `assignedTenantsCount`   | `Edm.Int32` | The total number of tenants assigned to the managementTemplateStepId. Required. Read-only. | No | Yes      | Yes      |
| `compliantTenantsCount`   | `Edm.Int32` | The number of compliant tenants assigned to the managementTemplateStepId. Required. Read-only.  | No | Yes      | Yes      |
| `notCompliantTenantsCount`   | `Edm.Int32` | The total number of not-compliant tenants assigned to the managementTemplateStepId. Required. Read-only.  | No | Yes      | Yes      |
| `dismissedTenantsCount`   | `Edm.Int32` | The number of dismissed tenants assigned to the managementTemplateStepId. Required. Read-only. | No | Yes      | Yes      |
| `ineligibleTenantsCount`   | `Edm.Int32` | The number of ineligible tenants assigned to the managementTemplateStepId. Required. Read-only. | No | Yes      | Yes      |

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managementTemplateStepTenantSummary",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplateStepTenantSummary",
  "id": "String (identifier)",
  "managementTemplateCollectionId": "String",
  "managementTemplateCollectionDisplayName": "String",
  "managementTemplateId": "String",
  "managementTemplateDisplayName": "String",
  "managementTemplateStepId": "String",
  "managementTemplateStepDisplayName": "String",
  "assignedTenantsCount": "Int32",
  "compliantTenantsCount": "Int32",
  "notCompliantTenantsCount": "Int32",
  "dismissedTenantsCount": "Int32",
  "ineligibleTenantsCount": "Int32",
  "createdDateTime": "DateTimeOffset",
  "createdByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "lastActionByUserId": "String"
}
```
