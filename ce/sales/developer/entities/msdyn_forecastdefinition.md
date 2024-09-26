---
title: "msdyn_forecastdefinition table/entity reference"
description: "Includes schema information and supported messages for the msdyn_forecastdefinition table/entity."
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

# msdyn_forecastdefinition table/entity reference

> [!NOTE]
> Unsure about table vs. entity? See [Developers: Understand terminology in Microsoft Dataverse](/powerapps/developer/data-platform/understand-terminology).

Defines the parameters used for forecasting.

**Added by**: Forecasting Solution


## Messages

|Message|Web API Operation|SDK class or method|
|-|-|-|
|Assign|PATCH /msdyn_forecastdefinitions(*msdyn_forecastdefinitionid*)<br />[Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) `ownerid` property.|<xref:Microsoft.Crm.Sdk.Messages.AssignRequest>|
|BulkRetain|This message is to be executed only by Dataverse to trigger registered plug-ins and flows.||
|Create|POST /msdyn_forecastdefinitions<br />See [Create](/powerapps/developer/data-platform/webapi/create-entity-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>|
|CreateMultiple|<xref:Microsoft.Dynamics.CRM.CreateMultiple?displayProperty=nameWithType />|<xref:Microsoft.Xrm.Sdk.Messages.CreateMultipleRequest>|
|Delete|DELETE /msdyn_forecastdefinitions(*msdyn_forecastdefinitionid*)<br />See [Delete](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-delete)|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>|
|GrantAccess|<xref:Microsoft.Dynamics.CRM.GrantAccess?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>|
|IsValidStateTransition|<xref:Microsoft.Dynamics.CRM.IsValidStateTransition?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>|
|ModifyAccess|<xref:Microsoft.Dynamics.CRM.ModifyAccess?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>|
|PurgeRetainedContent|This message is to be executed only by Dataverse to trigger registered plug-ins and flows.||
|Retain|This message is to be executed only by Dataverse to trigger registered plug-ins and flows.||
|Retrieve|GET /msdyn_forecastdefinitions(*msdyn_forecastdefinitionid*)<br />See [Retrieve](/powerapps/developer/data-platform/webapi/retrieve-entity-using-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>|
|RetrieveMultiple|GET /msdyn_forecastdefinitions<br />See [Query Data](/powerapps/developer/data-platform/webapi/query-data-web-api)|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>|
|RetrievePrincipalAccess|<xref:Microsoft.Dynamics.CRM.RetrievePrincipalAccess?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest>|
|RetrieveSharedPrincipalsAndAccess|<xref:Microsoft.Dynamics.CRM.RetrieveSharedPrincipalsAndAccess?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>|
|RevokeAccess|<xref:Microsoft.Dynamics.CRM.RevokeAccess?displayProperty=nameWithType />|<xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>|
|RollbackRetain|This message is to be executed only by Dataverse to trigger registered plug-ins and flows.||
|SetState|PATCH /msdyn_forecastdefinitions(*msdyn_forecastdefinitionid*)<br />[Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update) `statecode` and `statuscode` properties.|<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|
|Update|PATCH /msdyn_forecastdefinitions(*msdyn_forecastdefinitionid*)<br />See [Update](/powerapps/developer/data-platform/webapi/update-delete-entities-using-web-api#basic-update)|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>|
|UpdateMultiple|<xref:Microsoft.Dynamics.CRM.UpdateMultiple?displayProperty=nameWithType />|<xref:Microsoft.Xrm.Sdk.Messages.UpdateMultipleRequest>|
|ValidateRetentionConfig|This message is to be executed only by Dataverse to trigger registered plug-ins and flows.||

## Properties

|Property|Value|
|--------|-----|
|CollectionSchemaName|msdyn_forecastdefinitions|
|DisplayCollectionName|Forecast definitions|
|DisplayName|Forecast definition|
|EntitySetName|msdyn_forecastdefinitions|
|IsBPFEntity|False|
|LogicalCollectionName|msdyn_forecastdefinitions|
|LogicalName|msdyn_forecastdefinition|
|OwnershipType|UserOwned|
|PrimaryIdAttribute|msdyn_forecastdefinitionid|
|PrimaryNameAttribute|msdyn_forecastdefinitionname|
|SchemaName|msdyn_forecastdefinition|

<a name="writable-attributes"></a>

## Writable columns/attributes

These columns/attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [msdyn_fiscalmonth](#BKMK_msdyn_fiscalmonth)
- [msdyn_fiscalquarter](#BKMK_msdyn_fiscalquarter)
- [msdyn_fiscalyear](#BKMK_msdyn_fiscalyear)
- [msdyn_forecastdefinitionId](#BKMK_msdyn_forecastdefinitionId)
- [msdyn_forecastdefinitionname](#BKMK_msdyn_forecastdefinitionname)
- [msdyn_forecastperiodtype](#BKMK_msdyn_forecastperiodtype)
- [msdyn_metricid](#BKMK_msdyn_metricid)
- [msdyn_numberofrecurrences](#BKMK_msdyn_numberofrecurrences)
- [msdyn_quotasource](#BKMK_msdyn_quotasource)
- [msdyn_rollupquery](#BKMK_msdyn_rollupquery)
- [msdyn_validfrom](#BKMK_msdyn_validfrom)
- [msdyn_validto](#BKMK_msdyn_validto)
- [OverriddenCreatedOn](#BKMK_OverriddenCreatedOn)
- [OwnerId](#BKMK_OwnerId)
- [OwnerIdType](#BKMK_OwnerIdType)
- [statecode](#BKMK_statecode)
- [statuscode](#BKMK_statuscode)
- [TimeZoneRuleVersionNumber](#BKMK_TimeZoneRuleVersionNumber)
- [UTCConversionTimeZoneCode](#BKMK_UTCConversionTimeZoneCode)


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


### <a name="BKMK_msdyn_fiscalmonth"></a> msdyn_fiscalmonth

|Property|Value|
|--------|-----|
|Description|Select the fiscal month for the forecast definition.|
|DisplayName|Fiscal month|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_fiscalmonth|
|RequiredLevel|None|
|Type|Picklist|

#### msdyn_fiscalmonth Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|January||
|1|February||
|2|March||
|3|April||
|4|May||
|5|June||
|6|July||
|7|August||
|8|September||
|9|October||
|10|November||
|11|December||



### <a name="BKMK_msdyn_fiscalquarter"></a> msdyn_fiscalquarter

|Property|Value|
|--------|-----|
|Description|Select the fiscal quarter for the forecast definition.|
|DisplayName|Fiscal quarter|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_fiscalquarter|
|RequiredLevel|None|
|Type|Picklist|

#### msdyn_fiscalquarter Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|Q1||
|1|Q2||
|2|Q3||
|3|Q4||



### <a name="BKMK_msdyn_fiscalyear"></a> msdyn_fiscalyear

|Property|Value|
|--------|-----|
|Description|Select the fiscal year for the forecast definition.|
|DisplayName|Fiscal year|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_fiscalyear|
|RequiredLevel|None|
|Type|Picklist|

#### msdyn_fiscalyear Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|FY2018||
|1|FY2019||
|2|FY2020||
|3|FY2021||
|4|FY2022||
|5|FY2023||
|6|FY2024||
|7|FY2025||
|8|FY2026||
|9|FY2027||
|10|FY2028||
|11|FY2029||
|12|FY2030||
|13|FY2031||
|14|FY2032||
|15|FY2033||
|16|FY2034||
|17|FY2035||
|18|FY2036||
|19|FY2037||
|20|FY2038||
|21|FY2039||
|22|FY2040||



### <a name="BKMK_msdyn_forecastdefinitionId"></a> msdyn_forecastdefinitionId

|Property|Value|
|--------|-----|
|Description|Unique identifier for the forecast definition.|
|DisplayName|Forecast definition|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|msdyn_forecastdefinitionid|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|


### <a name="BKMK_msdyn_forecastdefinitionname"></a> msdyn_forecastdefinitionname

|Property|Value|
|--------|-----|
|Description|Name of the forecast definition.|
|DisplayName|Forecast name|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_forecastdefinitionname|
|MaxLength|100|
|RequiredLevel|ApplicationRequired|
|Type|String|


### <a name="BKMK_msdyn_forecastperiodtype"></a> msdyn_forecastperiodtype

|Property|Value|
|--------|-----|
|Description|Select the type of period for which the forecast must be generated.|
|DisplayName|Forecast period|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_forecastperiodtype|
|RequiredLevel|ApplicationRequired|
|Type|Picklist|

#### msdyn_forecastperiodtype Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|Monthly||
|1|Quarterly||
|2|Custom||



### <a name="BKMK_msdyn_metricid"></a> msdyn_metricid

|Property|Value|
|--------|-----|
|Description|Select metric to attach with forecast|
|DisplayName|Forecast metric|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_metricid|
|RequiredLevel|ApplicationRequired|
|Targets|metric|
|Type|Lookup|


### <a name="BKMK_msdyn_numberofrecurrences"></a> msdyn_numberofrecurrences

|Property|Value|
|--------|-----|
|Description|Indicate the number of recurrences that the forecast will be generated.|
|DisplayName|Number of recurrences|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_numberofrecurrences|
|MaxValue|12|
|MinValue|1|
|RequiredLevel|ApplicationRequired|
|Type|Integer|


### <a name="BKMK_msdyn_quotasource"></a> msdyn_quotasource

|Property|Value|
|--------|-----|
|Description|Select whether the quota for the forecast must to be taken from a goal or entered manually.|
|DisplayName|Quota source|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_quotasource|
|RequiredLevel|ApplicationRequired|
|Type|Picklist|

#### msdyn_quotasource Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|192350000|Goal-based||
|192350001|Manual||



### <a name="BKMK_msdyn_rollupquery"></a> msdyn_rollupquery

|Property|Value|
|--------|-----|
|Description|Select the query that will be used to calculate data for the rollup field.|
|DisplayName|Rollup query|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_rollupquery|
|RequiredLevel|None|
|Targets|goalrollupquery|
|Type|Lookup|


### <a name="BKMK_msdyn_validfrom"></a> msdyn_validfrom

|Property|Value|
|--------|-----|
|DateTimeBehavior|DateOnly|
|Description|Shows the date from which the forecast is applicable. The date and time are displayed in the time zone selected in Dynamics 365 Customer Engagement apps options.|
|DisplayName|Valid from|
|Format|DateOnly|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_validfrom|
|RequiredLevel|ApplicationRequired|
|Type|DateTime|


### <a name="BKMK_msdyn_validto"></a> msdyn_validto

|Property|Value|
|--------|-----|
|DateTimeBehavior|DateOnly|
|Description|Shows the date till which the forecast is applicable. The date and time are displayed in the time zone selected in Dynamics 365 Customer Engagement apps options.|
|DisplayName|Valid to|
|Format|DateOnly|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_validto|
|RequiredLevel|ApplicationRequired|
|Type|DateTime|


### <a name="BKMK_OverriddenCreatedOn"></a> OverriddenCreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time that the record was migrated.|
|DisplayName|Record Created On|
|Format|DateOnly|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|overriddencreatedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_OwnerId"></a> OwnerId

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Owner Id|
|DisplayName|Owner|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|ownerid|
|RequiredLevel|SystemRequired|
|Targets|systemuser,team|
|Type|Owner|


### <a name="BKMK_OwnerIdType"></a> OwnerIdType

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Owner Id Type|
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridtype|
|RequiredLevel|SystemRequired|
|Type|EntityName|


### <a name="BKMK_statecode"></a> statecode

|Property|Value|
|--------|-----|
|Description|Status of the Forecast Definition|
|DisplayName|Status|
|IsValidForCreate|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statecode|
|RequiredLevel|SystemRequired|
|Type|State|

#### statecode Choices/Options

|Value|Label|DefaultStatus|InvariantName|
|-----|-----|-------------|-------------|
|0|Draft|1|Draft|
|1|Published|2|Published|



### <a name="BKMK_statuscode"></a> statuscode

|Property|Value|
|--------|-----|
|Description|Reason for the status of the Forecast Definition|
|DisplayName|Status reason|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statuscode|
|RequiredLevel|None|
|Type|Status|

#### statuscode Choices/Options

|Value|Label|State|
|-----|-----|-----|
|1|Draft|0|
|2|In progress|1|
|3|Success|1|
|4|Failed|1|



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
- [CreatedByYomiName](#BKMK_CreatedByYomiName)
- [CreatedOn](#BKMK_CreatedOn)
- [CreatedOnBehalfBy](#BKMK_CreatedOnBehalfBy)
- [CreatedOnBehalfByName](#BKMK_CreatedOnBehalfByName)
- [CreatedOnBehalfByYomiName](#BKMK_CreatedOnBehalfByYomiName)
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedByName](#BKMK_ModifiedByName)
- [ModifiedByYomiName](#BKMK_ModifiedByYomiName)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [ModifiedOnBehalfByName](#BKMK_ModifiedOnBehalfByName)
- [ModifiedOnBehalfByYomiName](#BKMK_ModifiedOnBehalfByYomiName)
- [msdyn_metricidName](#BKMK_msdyn_metricidName)
- [msdyn_rollupqueryName](#BKMK_msdyn_rollupqueryName)
- [OwnerIdName](#BKMK_OwnerIdName)
- [OwnerIdYomiName](#BKMK_OwnerIdYomiName)
- [OwningBusinessUnit](#BKMK_OwningBusinessUnit)
- [OwningBusinessUnitName](#BKMK_OwningBusinessUnitName)
- [OwningTeam](#BKMK_OwningTeam)
- [OwningUser](#BKMK_OwningUser)
- [VersionNumber](#BKMK_VersionNumber)


### <a name="BKMK_CreatedBy"></a> CreatedBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user who created the record.|
|DisplayName|Created By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedByName"></a> CreatedByName

**Added by**: Active Solution Solution

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


### <a name="BKMK_CreatedByYomiName"></a> CreatedByYomiName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdbyyominame|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_CreatedOn"></a> CreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time when the record was created.|
|DisplayName|Created On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_CreatedOnBehalfBy"></a> CreatedOnBehalfBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the delegate user who created the record.|
|DisplayName|Created By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedOnBehalfByName"></a> CreatedOnBehalfByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_ModifiedBy"></a> ModifiedBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user who modified the record.|
|DisplayName|Modified By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedByName"></a> ModifiedByName

**Added by**: Active Solution Solution

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


### <a name="BKMK_ModifiedByYomiName"></a> ModifiedByYomiName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedbyyominame|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_ModifiedOn"></a> ModifiedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time when the record was modified.|
|DisplayName|Modified On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ModifiedOnBehalfBy"></a> ModifiedOnBehalfBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the delegate user who modified the record.|
|DisplayName|Modified By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedOnBehalfByName"></a> ModifiedOnBehalfByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_msdyn_metricidName"></a> msdyn_metricidName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|msdyn_metricidname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_rollupqueryName"></a> msdyn_rollupqueryName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|msdyn_rollupqueryname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_OwnerIdName"></a> OwnerIdName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Name of the owner|
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridname|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwnerIdYomiName"></a> OwnerIdYomiName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Yomi name of the owner|
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridyominame|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwningBusinessUnit"></a> OwningBusinessUnit

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the business unit that owns the record|
|DisplayName|Owning Business Unit|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|owningbusinessunit|
|RequiredLevel|None|
|Targets|businessunit|
|Type|Lookup|


### <a name="BKMK_OwningBusinessUnitName"></a> OwningBusinessUnitName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningbusinessunitname|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwningTeam"></a> OwningTeam

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the team that owns the record.|
|DisplayName|Owning Team|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningteam|
|RequiredLevel|None|
|Targets|team|
|Type|Lookup|


### <a name="BKMK_OwningUser"></a> OwningUser

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the user that owns the record.|
|DisplayName|Owning User|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owninguser|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_VersionNumber"></a> VersionNumber

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Version Number|
|DisplayName|Version Number|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|versionnumber|
|MaxValue|9223372036854775807|
|MinValue|-9223372036854775808|
|RequiredLevel|None|
|Type|BigInt|

<a name="onetomany"></a>

## One-To-Many Relationships

Listed by **SchemaName**.

- [msdyn_msdyn_forecastdefinition_msdyn_forecastinstance](#BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastinstance)
- [msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence](#BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence)


### <a name="BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastinstance"></a> msdyn_msdyn_forecastdefinition_msdyn_forecastinstance

Same as the [msdyn_msdyn_forecastdefinition_msdyn_forecastinstance](msdyn_forecastinstance.md#BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastinstance) many-to-one relationship for the [msdyn_forecastinstance](msdyn_forecastinstance.md) table/entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|msdyn_forecastinstance|
|ReferencingAttribute|msdyn_forecastdefinitionid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|msdyn_msdyn_forecastdefinition_msdyn_forecastinstance|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: 10000|
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence"></a> msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence

Same as the [msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence](msdyn_forecastrecurrence.md#BKMK_msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence) many-to-one relationship for the [msdyn_forecastrecurrence](msdyn_forecastrecurrence.md) table/entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|msdyn_forecastrecurrence|
|ReferencingAttribute|msdyn_forecastdefinitionid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|msdyn_msdyn_forecastdefinition_msdyn_forecastrecurrence|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: Unique identifier for Forecast Definition associated with Forecast Recurrence.<br />Order: 10000|
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|

<a name="manytoone"></a>

## Many-To-One Relationships

Each Many-To-One relationship is defined by a corresponding One-To-Many relationship with the related table. Listed by **SchemaName**.

- [msdyn_metric_msdyn_forecastdefinition_metricid](#BKMK_msdyn_metric_msdyn_forecastdefinition_metricid)
- [msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery](#BKMK_msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery)


### <a name="BKMK_msdyn_metric_msdyn_forecastdefinition_metricid"></a> msdyn_metric_msdyn_forecastdefinition_metricid

**Added by**: System Solution Solution

See the [msdyn_metric_msdyn_forecastdefinition_metricid](metric.md#BKMK_msdyn_metric_msdyn_forecastdefinition_metricid) one-to-many relationship for the [metric](metric.md) table/entity.

### <a name="BKMK_msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery"></a> msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery

**Added by**: System Solution Solution

See the [msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery](goalrollupquery.md#BKMK_msdyn_goalrollupquery_msdyn_forecastdefinition_rollupquery) one-to-many relationship for the [goalrollupquery](goalrollupquery.md) table/entity.

## Related information

[Dataverse table/entity reference](../about-entity-reference.md)  
[Web API Reference](/power-apps/developer/data-platform/webapi/reference/entitytypes)