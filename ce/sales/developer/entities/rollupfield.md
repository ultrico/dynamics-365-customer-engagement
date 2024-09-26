---
title: "RollupField table/entity reference"
description: "Includes schema information and supported messages for the RollupField table/entity."
ms.date: 02/27/2024
ms.service: "dynamics-365-sales"
ms.topic: "reference"
ms.assetid: 3948cc48-07c8-7f60-0608-71c37158ad7c
author: "lavanyakr01"
ms.author: lavanyakr
ms.reviewer: lavanyakr
search.audienceType: 
  - developer
---

# RollupField table/entity reference

> [!NOTE]
> Unsure about table vs. entity? See [Developers: Understand terminology in Microsoft Dataverse](/powerapps/developer/data-platform/understand-terminology).

Field to be rolled up to calculate the actual and in-progress values against the goal.


## Messages

|Message|Web API Operation|SDK class or method|
|-|-|-|
|Create|POST /rollupfields<br />See [Create](/powerapps/developer/data-platform/webapi/create-entity-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>|
|Delete|DELETE /rollupfields(*rollupfieldid*)<br />See [Delete](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-delete)|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>|
|Retrieve|GET /rollupfields(*rollupfieldid*)<br />See [Retrieve](/powerapps/developer/data-platform/webapi/retrieve-entity-using-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>|
|RetrieveMultiple|GET /rollupfields<br />See [Query Data](/powerapps/developer/data-platform/webapi/query-data-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>|
|Update|PATCH /rollupfields(*rollupfieldid*)<br />See [Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update)|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>|

## Properties

|Property|Value|
|--------|-----|
|CollectionSchemaName|RollupFields|
|DisplayCollectionName|Rollup Fields|
|DisplayName|Rollup Field|
|EntitySetName|rollupfields|
|IsBPFEntity|False|
|LogicalCollectionName|rollupfields|
|LogicalName|rollupfield|
|OwnershipType|None|
|PrimaryIdAttribute|rollupfieldid|
|PrimaryNameAttribute||
|SchemaName|RollupField|

<a name="writable-attributes"></a>

## Writable columns/attributes

These columns/attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [DateAttribute](#BKMK_DateAttribute)
- [EntityForDateAttribute](#BKMK_EntityForDateAttribute)
- [GoalAttribute](#BKMK_GoalAttribute)
- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [IsStateParentEntityAttribute](#BKMK_IsStateParentEntityAttribute)
- [MetricId](#BKMK_MetricId)
- [RollupFieldId](#BKMK_RollupFieldId)
- [SourceAttribute](#BKMK_SourceAttribute)
- [SourceEntity](#BKMK_SourceEntity)
- [SourceState](#BKMK_SourceState)
- [SourceStatus](#BKMK_SourceStatus)
- [TimeZoneRuleVersionNumber](#BKMK_TimeZoneRuleVersionNumber)
- [UTCConversionTimeZoneCode](#BKMK_UTCConversionTimeZoneCode)


### <a name="BKMK_DateAttribute"></a> DateAttribute

|Property|Value|
|--------|-----|
|Description|Select a date field for the selected record type, such as Actual Closed Date for the Opportunity record type. A record participates in the goal rollup, if the selected date falls between the start date and the end date for the goal.|
|DisplayName|Date Field|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|dateattribute|
|MaxLength|100|
|RequiredLevel|ApplicationRequired|
|Type|String|


### <a name="BKMK_EntityForDateAttribute"></a> EntityForDateAttribute

|Property|Value|
|--------|-----|
|Description|Select the record type that contains the date field that will be considered while rolling up data to the goal.|
|DisplayName|Record Type|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|entityfordateattribute|
|RequiredLevel|ApplicationRequired|
|Type|EntityName|


### <a name="BKMK_GoalAttribute"></a> GoalAttribute

|Property|Value|
|--------|-----|
|Description|Select a rollup field where the metric rollup data will be displayed in the goal. The options are an integer or money, depending on the Metric Type you chose for the goal metric.|
|DisplayName|Rollup Field|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|goalattribute|
|MaxLength|100|
|RequiredLevel|ApplicationRequired|
|Type|String|


### <a name="BKMK_ImportSequenceNumber"></a> ImportSequenceNumber

|Property|Value|
|--------|-----|
|Description|Sequence number of the import that created this record.|
|DisplayName|Import Sequence Number|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|importsequencenumber|
|MaxValue|2147483647|
|MinValue|-2147483648|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_IsStateParentEntityAttribute"></a> IsStateParentEntityAttribute

|Property|Value|
|--------|-----|
|Description|Tells whether the state or status belongs to the parent entity.|
|DisplayName|Is State/Status From Parent Entity|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|isstateparententityattribute|
|RequiredLevel|None|
|Type|Boolean|

#### IsStateParentEntityAttribute Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|1|Yes||
|0|No||

**DefaultValue**: 0



### <a name="BKMK_MetricId"></a> MetricId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the goal metric associated with the rollup field.|
|DisplayName|Goal Metric|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|metricid|
|RequiredLevel|ApplicationRequired|
|Targets|metric|
|Type|Lookup|


### <a name="BKMK_RollupFieldId"></a> RollupFieldId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the rollup field.|
|DisplayName|Rollup Field|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|rollupfieldid|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|


### <a name="BKMK_SourceAttribute"></a> SourceAttribute

|Property|Value|
|--------|-----|
|Description|Type the name of the field that the data for the goal rolls up from.|
|DisplayName|Source Field|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|sourceattribute|
|MaxLength|100|
|RequiredLevel|ApplicationRequired|
|Type|String|


### <a name="BKMK_SourceEntity"></a> SourceEntity

|Property|Value|
|--------|-----|
|Description|Type the name of the record type (entity) that the data for the goal must roll up from.|
|DisplayName|Source Record Type|
|IsValidForForm|True|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|sourceentity|
|RequiredLevel|ApplicationRequired|
|Type|EntityName|


### <a name="BKMK_SourceState"></a> SourceState

|Property|Value|
|--------|-----|
|Description|Select the state of the records you want to use as the source of the rollup data for the metric.|
|DisplayName|Source Record Type State|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|sourcestate|
|MaxValue|2147483647|
|MinValue|-2147483648|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_SourceStatus"></a> SourceStatus

|Property|Value|
|--------|-----|
|Description|Select the status of the records you want to use as the source of the rollup data for the metric.|
|DisplayName|Source Record Type Status|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|sourcestatus|
|MaxValue|2147483647|
|MinValue|-2147483648|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_TimeZoneRuleVersionNumber"></a> TimeZoneRuleVersionNumber

|Property|Value|
|--------|-----|
|Description|For internal use only.|
|DisplayName|Time Zone Rule Version Number|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|timezoneruleversionnumber|
|MaxValue|2147483647|
|MinValue|-1|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_UTCConversionTimeZoneCode"></a> UTCConversionTimeZoneCode

|Property|Value|
|--------|-----|
|Description|Time zone code that was in use when the record was created.|
|DisplayName|UTC Conversion Time Zone Code|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|utcconversiontimezonecode|
|MaxValue|2147483647|
|MinValue|-1|
|RequiredLevel|None|
|Type|Integer|

<a name="read-only-attributes"></a>

## Read-only columns/attributes

These columns/attributes return false for both **IsValidForCreate** or **IsValidForUpdate**. Listed by **SchemaName**.

- [CreatedBy](#BKMK_CreatedBy)
- [CreatedByName](#BKMK_CreatedByName)
- [CreatedOn](#BKMK_CreatedOn)
- [CreatedOnBehalfBy](#BKMK_CreatedOnBehalfBy)
- [CreatedOnBehalfByName](#BKMK_CreatedOnBehalfByName)
- [CreatedOnBehalfByYomiName](#BKMK_CreatedOnBehalfByYomiName)
- [MetricIdName](#BKMK_MetricIdName)
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedByName](#BKMK_ModifiedByName)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [ModifiedOnBehalfByName](#BKMK_ModifiedOnBehalfByName)
- [ModifiedOnBehalfByYomiName](#BKMK_ModifiedOnBehalfByYomiName)
- [OrganizationId](#BKMK_OrganizationId)
- [VersionNumber](#BKMK_VersionNumber)


### <a name="BKMK_CreatedBy"></a> CreatedBy

|Property|Value|
|--------|-----|
|Description|Shows who created the record.|
|DisplayName|Created By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedByName"></a> CreatedByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_CreatedOn"></a> CreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the record was created. The date and time are displayed in the time zone selected in Microsoft Dynamics 365 options.|
|DisplayName|Created On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_CreatedOnBehalfBy"></a> CreatedOnBehalfBy

|Property|Value|
|--------|-----|
|Description|Shows who created the record on behalf of another user.|
|DisplayName|Created By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedOnBehalfByName"></a> CreatedOnBehalfByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdonbehalfbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_CreatedOnBehalfByYomiName"></a> CreatedOnBehalfByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdonbehalfbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_MetricIdName"></a> MetricIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|metricidname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedBy"></a> ModifiedBy

|Property|Value|
|--------|-----|
|Description|Shows who last updated the record.|
|DisplayName|Modified By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedByName"></a> ModifiedByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedOn"></a> ModifiedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the record was last updated. The date and time are displayed in the time zone selected in Microsoft Dynamics 365 options.|
|DisplayName|Modified On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ModifiedOnBehalfBy"></a> ModifiedOnBehalfBy

|Property|Value|
|--------|-----|
|Description|Shows who last updated the record on behalf of another user.|
|DisplayName|Modified By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedOnBehalfByName"></a> ModifiedOnBehalfByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedOnBehalfByYomiName"></a> ModifiedOnBehalfByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_OrganizationId"></a> OrganizationId

|Property|Value|
|--------|-----|
|Description|Choose the ID of the organization that the record is associated with.|
|DisplayName|Organization Id|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|organizationid|
|RequiredLevel|None|
|Targets||
|Type|Lookup|


### <a name="BKMK_VersionNumber"></a> VersionNumber

|Property|Value|
|--------|-----|
|Description|Version number of the rollup field.|
|DisplayName|Version Number|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|versionnumber|
|MaxValue|9223372036854775807|
|MinValue|-9223372036854775808|
|RequiredLevel|None|
|Type|BigInt|

<a name="manytoone"></a>

## Many-To-One Relationships

Each Many-To-One relationship is defined by a corresponding One-To-Many relationship with the related table. Listed by **SchemaName**.


### <a name="BKMK_metric_rollupfield"></a> metric_rollupfield

See the [metric_rollupfield](metric.md#BKMK_metric_rollupfield) one-to-many relationship for the [metric](metric.md) table/entity.

## Related information

[Dataverse table/entity reference](../about-entity-reference.md)  
[Web API Reference](/power-apps/developer/data-platform/webapi/reference/entitytypes)