---
title: "Enhanced Collaboration for Microsoft Teams with Dynamics 365 app"
description: "Learn how to use Enhanced Collaboration with Microsoft Teams, and connect a record or view to a team channel from Dynamics 365 customer engagement apps."
ms.date: 08/16/2024
ms.topic: article
author: sbmjais
ms.author: shjais
ms.reviewer: shjais 
ms.custom: 
search.audienceType: 
  - enduser
applies_to: 
  - Dynamics 365 apps
ms.assetid: 8097c9ec-023b-407d-ac0e-074b5e1964a5
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 1
---

# Enhanced collaboration experience with the Dynamics 365 app for Microsoft Teams

This article provides information on how to use enhanced collaboration with Microsoft Teams, and connect a record or view to a team channel from Dynamics 365 customer engagement apps.

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | <ul><li>Dynamics 365 Sales Premium, Dynamics 365 Sales Enterprise, Dynamics 365 Sales Professional, Dynamics 365 Team Members, or any Dynamics 365 customer engagement app license</li> <li>Microsoft Teams license</li></ul>  <br>More information: <ul><li>[Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/)</li><li>[Microsoft Teams pricing](https://www.microsoft.com/microsoft-teams/compare-microsoft-teams-options?activetab=pivot:primaryr2&rtc=1)</li><li>[Dynamics 365 Team Members](/dynamics365/get-started/team-members-license)</li><li>[Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409)</li></ul> |
| **Security roles** | <ul><li>Any primary sales role, such as salesperson, or sales manager</li><li>Any role that has access to a Dynamics 365 record</li></ul> <br>  More information: [Primary sales roles](../security-roles-for-sales.md#primary-sales-roles)|

## Overview

Easily connect customer engagement apps in Dynamics 365 (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, or Dynamics 365 Project Service Automation) records or views to a Microsoft Teams channel using the **Collaborate** button on the record or view page. The step-by-step process helps you connect the selected record or view to a Microsoft Teams channel.

The [basic collaboration experience](teams-collaboration.md) only lets you pin a record or a view to a team channel from within Microsoft Teams. The enhanced collaboration experience includes everything in the [basic collaboration experience](teams-collaboration.md) and also lets your pin connect a record or a view to a team channel while you're working in customer engagement apps in Dynamics 365 (such as Dynamics 365 Sales and Dynamics 365 Customer Service). 

## Connect a record or a view to a team channel from customer engagement apps in Dynamics 365

1. In customer engagement apps (such as Dynamics 365 Sales or Dynamics 365 Customer Service), open a record or a view.
2. On the command bar, select **Collaborate**.

    :::image type="content" source="media/teams-collorate-option_1.png" alt-text="Screenshot of the Collaborate option in Dynamics 365 app.":::

3. On the **Collaborate with Microsoft Teams** window, you'll see one of the following: 
    - **If there’s no channel**: You can connect the current record or view to any team channel by selecting, **Get started**.

        :::image type="content" source="media/teams-get-started-2.png" alt-text="Screenshot of the Get Started button.":::

    - **If there is channel that's already connected**: Select a channel from the list and then select, **Start collaboration**. This opens Microsoft Teams and navigate to the channel that you selected. Or, connect the current record or view to a new team channel by selecting, **Create a new connection**.

        :::image type="content" source="media/teams-existing-channel-screen-note.png" alt-text="Screenshot of the screen to select an existing channel.":::

     > [!NOTE]
     >  If you selected an existing connected team channel where you are not the owner or member in that team, then when Microsoft Teams opens, select **Join** to send request to be added to the channel. 

4. After you select **Get started** or **Create a new connection**, you'll enter into the connection process. 

   **Step 1**: Choose an existing team or create a new team.
   
   - Choose an existing team that you belong to and then select **Next**.

      :::image type="content" source="media/teams-add-to-existing-team-3.png" alt-text="Screenshot of the screen to select a team.":::

   - Or, create a new team:  

        1. Select **Create new team** at the bottom of the list.

        2. Enter a name for the team and then select **Next**. </br>
           If your administrator has enabled sensitivity labels for Teams, you'll see the **Sensitivity** field. Select a **Sensitivity** label from the list. Hover over the label to see tooltips to get more information about the label. Select **Make it a private  team** to ensure that only the team owner can add more members.  
                
            :::image type="content" source="media/teams-enter-team-name-5.png" alt-text="Screenshot of entering a team name and selecting next.":::


   **Step 2**: Choose an existing channel and then select **Next**, or select **Create new channel** to create a new channel.

      :::image type="content" source="media/teams-choose-channel.png" alt-text="Screenshot of choosing a channel.":::

      > [!NOTE]
      > When you create a new team, the system automatically creates a channel named **General**. You can connect the current record to the **General** channel and then select **Next** or select **create new channel** to create a new channel under the newly created team.

   **Step 3**: If you're the owner of the selected team, then you can add recommended teammates who either own the record or the record has been shared with them to the team member group. From the list, select any or all listed teammates. You can also use the search option to find the teammates in the list. When you're done, select **Finish**.

   > [!NOTE]
   > You will see this step only if you are the owner of the selected team while connecting to a customer engagement app record. If you are connecting a view of customer engagement app to a Microsoft Teams channel, you will skip this step. For more information on how to share a record, see [Assign or share records.](/powerapps/user/assign-or-share-records).

    :::image type="content" source="media/teams-choose-teammates-7.png" alt-text="Screenshot of choosing teammates.":::

5. When the connection process is complete, the system opens Microsoft Teams and go to channel that you connected.

## Related information

[Enable sensitivity labels to protect content in Microsoft Team](sensitivity-labels.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

