---
title: "Basic navigation in App for Outlook (Dynamics 365 apps) | MicrosoftDocs"
description: How to navigate App for Outlook
ms.custom: 
ms.date: 10/12/2023
ms.reviewer: sericks
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: Dynamics 365 apps
caps.latest.revision: 1
author: sidhartg
ms.author: sidhartg
search.audienceType: 
  - admin
  - customizer
  - enduser
contributors:
- sbmjais
---

# Basic navigation in App for Outlook

Use Dynamics 365 App for Outlook while you’re using Outlook on the desktop, web, or phone. When App for Outlook is installed you can use the Dynamics 365 pane to link and track Outlook emails and appointments to records in your app.

> [!IMPORTANT]
> - The latest release of Dynamics 365 App for Outlook works with customer engagement apps (such as [Dynamics 365 Sales](../../sales-professional/help-hub.md), [Dynamics 365 Customer Service](../../customer-service/help-hub.md), [Dynamics 365 Marketing](../../marketing/help-hub.yml). [Dynamics 365 Field Service](../../field-service/overview.md), and [Dynamics 365 Project Service Automation](/dynamics365/project-operations/psa/overview)), [Dynamics 365 Customer Engagement (on-premises), version 9](../../customerengagement/on-premises/overview.md), and [Microsoft Dataverse](/powerapps/maker/common-data-service/data-platform-intro).
> - For a prior release that works with earlier versions of Dynamics 365 apps, see [Deploy Dynamics 365 App for Outlook](/previous-versions/dynamicscrm-2016/administering-dynamics-365/dn946901(v=crm.8)). 


## Install 

Before installing App for Outlook, contact your administrator and make sure all the prerequisites are met. For more information, see [Deploy Dynamics 365 App for Outlook](../deploy-dynamics-365-app-for-outlook.md).

In most cases, your administrator will automatically push the app to you and it should be available in the Outlook ribbon. If you don't see it, then you can install it yourself. For more information, see [Have users install App for Outlook themselves](../deploy-dynamics-365-app-for-outlook.md#have-users-install-app-for-outlook-themselves).


## Access the app and sign in

Once installed it's easy to access the Dynamics 365 App for Outlook pane whether you're using Outlook on your desktop or the web app.

- In the Outlook desktop client, select **Dynamics 365**.

   > [!div class="mx-imgBorder"] 
   > ![Open App for Outlook pane.](../media/open-pane-appforoutlook.png)  
   
- In Outlook Web Access, open an email and then select More (...) > **Dynamics 365**.

   > [!div class="mx-imgBorder"] 
   > ![Open App for Outlook pane in Outlook Web Access.](../media/outlook-web-app.png)

When you first access the Dynamics 365 App for Outlook pane, you are prompted to sign in to your Dynamics 365 account. In the confirmation message, select **Allow** and then follow the steps on screen to sign in to Dynamics 365. After you have signed in, as long as you use the app frequently, you'll remain signed in. If you haven't used the app for 90 days, you will be asked to sign in again. 

   
## Pin 

If you're using the Outlook desktop client or Outlook Web Access, you can pin App for Outlook so that it remains open when you navigate from one email to another. If you don't see the pin option, then verify that it's supported for your setup. For more information, see [What's supported](support-matrix.md).

- To pin the app, select the pin. To unpin, select the pin again.

   > [!div class="mx-imgBorder"] 
   > ![Pin the add-in.](../media/pin-addin.gif)  


## Terminology

|Term  |Definition  |
|---------|---------|
|[Set regarding](track-message-or-appointment.md)     |Track and link the email or appointment to an existing row your Dynamics 365 app.|
|[Track](track-message-or-appointment.md)     |Create a copy of the email or appointment in your Dynamics 365 app.   |
|[Untrack](track-message-or-appointment.md#untrack-a-linked-email-or-appointment)     |Remove the copy of the email or appointment from your Dynamics 365 app. |
|Track Successful |Your email or appointment is successfully copied to  your Dynamics 365 app.   |
|Track failure |Your email or appointment is failed to copy to your Dynamics 365 app.   | 
|Track pending |Your email or appointment is in pending state to be copied to your Dynamics 365 app.   | 


## Navigation bar

Use the navigation bar at the top to access the site map, search, quick create, and more commands.

![Top navigation bar.](../media/top-nav-bar.png)

1. **Site map**: Use the site map to navigate to the **Home**, **Recent** items, **Pinned** items, and **Dashboards**.
2. **Search**: Search for rows across multiple tables sorted by relevance. 
3. **Create a new row**: Create a new row for the tables that have been included in the App for Outlook and are enabled for quick create.
4. **More commands**: Access more such as user information, information your Dynamics 365 environment, the [**Assistant**](assistant.md), and [**Outlook checker**](../diagnostic-checker.md).
5. **Pin**: Select the pin icon to pin Dynamics 365 App pane so that it remains open when you navigate from one email to another.



## Site map

Use the site map to navigate to **Home**, **Recent** items, **Pinned** items, and **Dashboards**.

![Open the site map menu.](../media/site-map-menu.gif)

### Site map menu items

It's easy to get around and get back to your favorite or most-used rows. The following illustration shows the primary navigation elements

![Menu items in the site map.](../media/site-map-menu-items.png)


Legend

1. **Home**: Take you to the Dynamics 365 App for Outlook main screen that displays tracking status, the regarding row with contextual information.
2. **Recent**: Expand this entry to view a list of rows you were recently using. Select a row here to open it. Select the push-pin icon next to a row listed here to add it to your pinned rows.
3. **Pinned**: Expand this entry to view and open your favorite pinned rows. Use the **Recent** list to add rows here. Select the remove-pin icon next to a row listed here to remove it from this list.


## Tracked row

Select an email to view additional information about the tracked item in the Dynamics 365 pane.

![Additional information when an email is tracked.](../media/tracked-item.png)

Legend

1. **Linked row information**: The Dynamics 365 row this Outlook item is linked to. The quick view form displays some of the row's key information.
2. **Recipients**: List of recipients from the email or the attendees of a meeting. You can navigate between the different recipients, which can be a contact, lead, or an account and display a quick view of their information in Dynamics 365. 
3. **Related information**: When a contact is selected, its parent account is also available so you can drill into the account details and surface more Dynamics 365 data. You can also see related data, such as related the contact's opportunities.


![See mpre information about a tracked row.](../media/tracked-item-more-info.png)


1. **Tracked information**: Shows if the email message or meeting is linked to a row and if it's being tracked in your Dynamics 365 app.

2. **More commands**: Select to set or change set regarding or tracking information or view information about the row in Dynamics 365

3. **Add activity**: Select to create activities for that row or view it in Dynamics 365.

4 & 5. **Set regarding**: Select to choose the **Set regarding** for the row or view information about the row in Dynamics 365.


