---
title: Define status reason transitions for case management (Dynamics 365 Customer Service) | MicrosoftDocs
description: Understand how to define status reason transitions for case management in Customer Service.
ms.date: 12/21/2023
ms.topic: article
author: neeranelli
ms.author: nenellim
search.audienceType: 
  - admin
  - customizer
  - enduser
ms.custom: 
  - dyn365-customerservice
---

# Define status reason transitions for case management

If you’re in charge of incident management for an organization, it’s important to provide a model for agents to enter and update case status. In Dynamics 365 Customer Service, there are two fields in the Case table that provide information about case status: the **Status** field and the **Status Reason** field. The **Status** field for the **Case** entity has three possible values: **Active**, **Resolved**, or **Canceled**. The **Status Reason** field stores a reason for a specific status value. For example, for a case with an **Active** status, a status reason could be **In Progress**, **On Hold**, **Waiting for Details**, or **Researching**.  

 Organizations often have a large number of combinations for the **Status** and **Status Reason** fields. This can make it difficult for agents to choose the correct next status reason. You can define status reason transitions to add another level of filtering for what the status reason value can be changed to for each status reason. Limiting these values to the allowed status reasons can help customer service representatives make the right choices.  

## Prerequisites
  
[!INCLUDE[proc_permissions_system_admin_and_customizer](../../includes/proc-permissions-system-admin-and-customizer.md)]  

## Add status reason transitions

1. In [Power Apps](https://make.powerapps.com/), select your environment.
1. Select **Tables** and then select **Case**.
1. Select **Columns** and then select **Status Reason**.
1. In the **Edit column** pane, select the required status from the dropdown. Select **New choice** to add the required status reason transition.
1. Specify the **Default choice** dropdown. This is the default value that appears on the case form for the **Status Reason** field.
1. Select **Save**.

   :::image type="content" source="../media/powerapps-case-resol-add-value.png" alt-text="Screenshot displaying powerapps configuration":::

### Related information

[Edit the column](/power-apps/maker/data-platform/create-edit-field-portal#edit-a-column)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
