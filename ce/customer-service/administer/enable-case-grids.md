---
title: Enable case grids for agents
description: Learn how you can enable case grids and increase agent productivity.
ms.date: 08/01/2024
ms.topic: article
author: Soumyasd27
ms.author: sdas
search.audienceType: 
  - admin
  - customizer
  - enduser
ms.custom: 
  - dyn365-customerservice
ms.collection: get-started
---

# Enable case grids

Increase your agent's productivity by providing quick access to information, such as the last customer interaction, case age, and the next SLA breach, with modernized case grids. The modern UI presents data in an intuitive manner that helps you and your agents perform inline edits and quick operations with minimal clicks, facilitating decision-making.

## Key features

The following are some of the key features of the modernized case grids:

- A view called **Enhanced Active Cases**, which includes a set of predefined columns where you can:
    - View icons for **Priority** and the **Origin** channel.
    -	View avatars for the assigned **Owner**.
    - View key data, such as **Case Age**, **Next SLA**, and **Last Interaction** with attachments.
- The ability to perform inline edits and update data for columns. For example, you can double-click the **Priority** column to change the priority of the case or set the toggle to **Yes** or **No** in the **Is Escalated** column. The updated data is automatically saved only when you move to the next row. Currently, inline editing for the **Status reason** column isn't supported.

- The ability to use quick navigation to respond to the latest interaction.

> [!NOTE]
> - If you [opt in](/power-platform/admin/opt-in-early-access-updates) to early access features, agents will see the following by default:
>   - The **Enhanced Active Cases** view with additional fields, **Case Age**, **Next SLA**, **Is escalated**, and **Last Interaction**. 
>   - Color coded icons for **Priority** and the **Origin** channels, avatars for **Owner** appear in all the case views.

## Enable the grid control for the Case entity

> [!NOTE]
> - If you [opt in](/power-platform/admin/opt-in-early-access-updates) to early access features, the following actions apply:
>    - The **Enhanced Active Cases** view is enabled by default for the **Case** entity. However, edit actions aren't enabled by default. To allow agents to perform inline edits and update data for columns in the view, turn on **Configure property Enable Editing** in Power Apps.
>    - **Power Apps grid control** option is enabled by default for the **Case** entity and replaces the out-of-the-box legacy grids. 
>    - If you want to revert to the legacy grids, enable the **Read-only Grid(default)** option in the **Controls** section of the **Case** entity in Power Apps.
>    - If you are using grids that aren't available out of the box, they won't be replaced by the **Power Apps grid control**.

If you haven't opted in to the early access features, you must enable the **Power Apps grid control** option on the Power Apps portal to make the **Enhanced Active Cases** view accessible to agents.

1. Go to the https://make.powerapps.com. portal.
1. Select **Solutions**. The **Solutions** page appears.
1. On the **Solutions** page, select **Default Solution**.
1. On the left pane on the **Default Solution** page, select **Tables**, and then select **Case**.
1. Select **Switch to classic**.
1. On the **Case** page, in the **Controls** section, select **Add Control**.
1. In the **Add Control** dialog, select **Power Apps grid control** > **Add**.
1. On the **Controls** tab, do the following:

    1. In the **Controls** section, for **Power Apps grid control**, select **Web**, **Phone**, and **Tablet** radio button/options.
    1. In the **Property** section in the **Customizer Control** field, select **Edit**. The **Configure property “Customizer Control Name”** dialog appears.
    1. In the **Configure property “Customizer Control Name”** dialog, select **Bind to a static value option**. For **Single line.Text**, select **MscrmControls.CustomCellControl.CustomCellControl**, and then select **OK**.
     1. To enable inline editing, do the following:
       1. In the **Property** section in **Enable editing**, select **Edit**. The **Configure property Enable Editing** dialog appears.
       1. In the **Configure property Enable Editing** dialog, select **Bind to static options**, select **Yes** from the dropdown list, and then select **OK**.
     1. Set **Enable OptionSet colors** to **Yes** to display color coded case status fields.
     > [!NOTE]
     > Any changes made by Microsoft to the default color palette won't be available automatically if you've customized the colors that appear on the case status field.
1. Select **Save**, and then select **Publish**.

## Enable the Enhanced Active Cases view in Customer Service workspace

To make the **Enhanced Active Cases** view accessible to agents in Customer Service workspace:

 1. Go to your environment by using your organization link.
 
 1. In the Customer Service Workspace Model Driven App, from the list of apps, select **More Options**, and then select **Open in App Designer**.
  1. Go to **Components > Entity Assets > Views**, and then select the **Case** entity.
  1. On the Components tab, search for **Enhanced Active Cases** view, and then select the checkbox.
  1. Select **Save**, and then select **Publish**.

## Customize the case grid

### Add columns to the case grid

1. Go to the https://make.powerapps.com portal.

1. Select **Solutions**. The **Solutions** page appears.
1. On the **Solutions** page, select **Default Solution**.
1. On the left pane on the **Default Solution** page, select **Tables**, and then select **Case**.
1. On the **Case** page, select **Views**.
1. Select the case type that you want to update, for example, **All Cases**.
1. On the **View** page, select **+ View** column.
1. In the **View column** dialog, search for the column that you want to add&mdash;for example, the **Last Interaction** column. The **Last Interaction** column now appears on the **View** page.
1. Select **Save**, and then select **Publish**.

### Add new icons for Origin and Priority Columns

In the following example, you add a new **Option Set Value** for the **Priority** and **Origin** column.

1. Go to https://make.powerapps.com portal.
1. Select **Solutions**.
1. Select the solution in which you want to add the web resource. 
1. Select **New** > **More** > **Web resource**.
1. In the **New web resource** dialog, enter the following:

   1. Upload your file by selecting the **Upload file** option.
   1. In the **Display name** field, enter a display name.
   1. In the **Name** field, enter the name in the format: **Incident/Priority/{Option Set Value}PriorityIcon.{File Extension}** or **Incident/Origin/{Option Set Value}OriginIcon.{File Extension}**. For example, **Incident/Priority/100000000PriorityIcon.png**.
1. Select **Save**.

### Related information

[Enable entities for service-level agreements](enable-entities-service-level-agreements.md)
  
[Troubleshoot issues in SLAs](../troubleshoot-sla-issues.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
