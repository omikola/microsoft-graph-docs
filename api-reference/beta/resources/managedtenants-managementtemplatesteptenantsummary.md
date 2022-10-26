---
title: "managementTemplateStepTenantSummary resource type"
description: "Represents the summary of a managementTemplateStep on a tenant."
author: "oliviamikola"
ms.localizationpriority: medium
ms.prod: "microsoft-365-lighthouse"
doc_type: resourcePageType
---

# managementTemplateStepTenantSummary resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the summary of a [managementTemplateStep](../resources/managedtenants-managementtemplatestep.md) on a tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managementTemplateStepTenantSummaries](../api/managedtenants-managedtenant-list-managementtemplatesteptenantsummaries.md)|[microsoft.graph.managedTenants.managementtemplatesteptenantsummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) collection|Get a list of the [microsoft.graph.managedTenants.managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) objects and their properties.|
|[Get managementTemplateStepTenantSummary](../api/managedtenants-managementtemplatesteptenantsummary-get.md)|[microsoft.graph.managedTenants.managementtemplatesteptenantsummary](../resources/managedtenants-managementtemplatesteptenantsummary.md)|Read the properties and relationships of a [microsoft.graph.managedTenants.managementTemplateStepTenantSummary](../resources/managedtenants-managementtemplatesteptenantsummary.md) object.|

## Properties
| Property                                | Type           | Description                                                                                                                                                                                                     |
|:----------------------------------------|:---------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id                                      | String         | The unique identifier for the entity. Required. Read-only.                                                                                                                                                      |
| createdDateTime                         | DateTimeOffset | The date and time when this entity was created. Required. Read-only.                                                                                                                                            |
| createdByUserId                         | String         | The unique identifier for the Azure Active Directory (Azure AD) user who created this entity. Required. Read-only.                                                                                              |
| lastActionDateTime                      | DateTimeOffset | The date and time at which this entity was last modified. Normally caused by activities in the related [managementTemplateCollections](../resources/managedtenants-managementtemplatecollection.md). Read-only. |
| lastActionByUserId                      | String         | The unique identifier for the Azure AD user who last modified this entity. Normally caused by activities in the related **managementTemplateCollections**. Read-only.                                           |
| managementTemplateCollectionId          | String         | The unique identifier for the **managementTemplateCollection** associated with this summary. Required. Read-only.                                                                                               |
| managementTemplateCollectionDisplayName | String         | The **managementTemplateCollection** display name associated with this summary. Required. Read-only.                                                                                                            |
| managementTemplateId                    | String         | The unique identifier for the [managementTemplate](../resources/managedtenants-managementtemplate.md) associated with this summary. Required. Read-only.                                                        |
| managementTemplateDisplayName           | String         | The **managementTemplate** display name associated with this summary. Required. Read-only.                                                                                                                      |
| managementTemplateStepId                | String         | The unique identifier for the **managementTemplateStep** associated with this summary. Required. Read-only.                                                                                                     |
| managementTemplateDisplayName           | String         | The **managementTemplateStep** display name associated with this summary.  Required. Read-only.                                                                                                                 |
| assignedTenantsCount                    | Int32          | The total number of tenants assigned to the **managementTemplateStepId**. Required. Read-only.                                                                                                                  |
| compliantTenantsCount                   | Int32          | The number of compliant tenants assigned to the **managementTemplateStepId**. Required. Read-only.                                                                                                              |
| notCompliantTenantsCount                | Int32          | The total number of not-compliant tenants assigned to the **managementTemplateStepId**. Required. Read-only.                                                                                                    |
| dismissedTenantsCount                   | Int32          | The number of dismissed tenants assigned to the **managementTemplateStepId**. Required. Read-only.                                                                                                              |
| ineligibleTenantsCount                  | Int32          | The number of ineligible tenants assigned to the **managementTemplateStepId**. Required. Read-only.                                                                                                             |

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
 json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplateStepTenantSummary",
  "assignedTenantsCount": "Int32",
  "compliantTenantsCount": "Int32",
  "createdByUserId": "String",
  "createdDateTime": "DateTimeOffset",
  "dismissedTenantsCount": "Int32",
  "id": "String (identifier)",
  "ineligibleTenantsCount": "Int32",
  "lastActionByUserId": "String",
  "lastActionDateTime": "DateTimeOffset",
  "managementTemplateCollectionDisplayName": "String",
  "managementTemplateCollectionId": "String",
  "managementTemplateDisplayName": "String",
  "managementTemplateId": "String",
  "managementTemplateStepDisplayName": "String",
  "managementTemplateStepId": "String",
  "notCompliantTenantsCount": "Int32"
}
