---
title: IoT - Parent IoT Alerts workflow
description: "Links potential redundant IoT alerts to an existing parent alert."
ms.date: 03/15/2024
ms.topic: conceptual
ms.author: vhorvath
author: vhorvathms
search.audienceType: 
  - developer
ms.custom: 
  - dyn365-developer
  - dyn365-fieldservice
---

# IoT - Parent IoT Alerts workflow

The **IoT - Parent IoT Alerts** workflow links potential redundant alerts to an existing parent alert.  

> [!NOTE]
> The Web API types and operations mentioned in this article/table are available in your environment and you can use the service document of your environment or Insomnia to explore these types and operations. More information: [Web API Service Documents](/power-apps/developer/data-platform/webapi/web-api-service-documents) and [Use Insomnia with Microsoft Dataverse Web API](/power-apps/developer/data-platform/webapi/insomnia).
  
Calls the `Microsoft.Dynamics.CRM.msdyn_ParentIoTAlerts` API and passes 60 for the `TimespanSeconds` parameter. The primary entity for this workflow is `msdyn_iotalert`.
  
This workflow is an example that ships with the thermostat sample solution. It demonstrates how to handle duplicate/redundant alerts to [!INCLUDE[pn_dyn_365](../includes/pn-dyn-365.md)], which typically occurs when a device malfunctions.  It's a recommended best practices approach, because unfiltered alerts can result in unwanted duplicated remedial processing. For example, multiple, redundant reset commands sent or work orders generated. Redundant actions can also negatively affect the performance of your [!INCLUDE[pn_dyn_365](../includes/pn-dyn-365.md)] instance. (The thermostat sample is coded to filter duplicate alerts so that they aren't passed to [!INCLUDE[pn_dyn_365](../includes/pn-dyn-365.md)], which is also a recommended practice.)  
  
This workflow is enabled by default. Users can edit or deactivate it.  

## Parameters

 Parameter(s) allow for data to be passed to the workflow.  
  
|Name|Type|Nullable|Unicode|Description|  
|----------|----------|--------------|-------------|-----------------|  
|TimespanSeconds|Edm.Int32|false||Determines the time window to consider when parenting (or suppressing) an alert, from 60 to 180 seconds.|
| | | | | |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
