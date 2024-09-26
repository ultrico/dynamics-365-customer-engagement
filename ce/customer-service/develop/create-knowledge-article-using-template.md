---
title: Create a knowledge article using a template (Developer Guide for Dynamics 365 Customer Service)
description: Read how you can create a knowledge article from an existing template using msdyn_GetKAObjectFromTemplate action.
ms.date: 07/24/2024
ms.topic: article
author: Soumyasd27
ms.author: sdas
ms.reviewer: sdas
ms.custom: 
  - dyn365-customerservice
  - bap template
search.audienceType: 
  - developer
---
# Create a knowledge article using a template

Use the **msdyn_GetKAObjectFromTemplate** action to create a knowledge article from an existing knowledge article template programmatically.

## Action parameters

The **msdyn_GetKAObjectFromTemplate** action requires the following parameters:

| Name | Type | Nullable | Description |
| ---- | ---- | ---- | ---- |
| TemplateId | Edm.Guid | False | The GUID of the knowledge article template to use. |

## Action return type

| Type | Description |
| ---- | ---- |
| [KnowledgeArticle](../../customerengagement/on-premises/developer/entities/knowledgearticle.md) | The **msdyn_GetKAObjectFromTemplate** action returns the following value. |

## Example

**Request**

```http
POST [Organization URI]/api/data/v9.0/msdyn_GetKAObjectFromTemplate
Content-Type: application/json;charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "TemplateId":"{A2AC047C-507D-E911-A828-000D3A1C16AF}"
}
```

**Response**

```json
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{
    "@odata.context":"[Organization URL]/api/data/v9.0/$metadata#knowledgearticles/$entity",
    "@odata.type":"#Microsoft.Dynamics.CRM.knowledgearticle",
    "isinternal":false,
    "isinternal@OData.Community.Display.V1.FormattedValue":"No",
    "keywords":"test knowledge article",
    "title":"test",
    "_languagelocaleid_value":"56940b3e-300f-4070-a559-5a6a4d11a8a3",
    "_languagelocaleid_value@Microsoft.Dynamics.CRM.associatednavigationproperty":"languagelocaleid",
    "_languagelocaleid_value@Microsoft.Dynamics.CRM.lookuplogicalname":"languagelocale",
    "_subjectid_value":"8069216f-297d-e911-a828-000d3a53e137",
    "_subjectid_value@Microsoft.Dynamics.CRM.associatednavigationproperty":"subjectid",
    "_subjectid_value@Microsoft.Dynamics.CRM.lookuplogicalname":"subject",
    "_subjectid_value@OData.Community.Display.V1.FormattedValue":"Query"
}
```

### Related information

[Search for knowledge articles in the Customer Service Hub](../use/search-knowledge-articles-csh.md)  
[Create and manage knowledge articles](../use/customer-service-hub-user-guide-knowledge-article.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
