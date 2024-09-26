---
title: Manage bookmarks for reports
description: Learn how to create bookmarks to save personalized views of your Dynamics 365 Customer Service reports, set a bookmark as your default view, and delete bookmarks you no longer need.
author: Soumyasd27
ms.author: sdas
ms.reviewer: sdas
ms.topic: how-to
ms.date: 05/10/2024
ms.custom: bap-template
---

# Manage bookmarks for reports

[!INCLUDE[cc-feature-availability](../../includes/cc-feature-availability.md)]


A bookmark captures the state of a report page, including changes that you've made to the filters. Personalize your reports and save the time and effort required to reapply the filters every time you want to view specific data. Use bookmark options to select a saved view, update or delete a bookmark, and set a bookmark as your default view.

A bookmark that you create for a [report group](report-filters-groups.md) saves a personalized view using that group's filters. For example, if you create a bookmark in the Omnichannel historical report's **Conversation** tab, the bookmark applies to the **Conversation**, **Queue**, and **Agent** tabs, and doesn't include filters for the other tabs.

You can use bookmarks in all the out-of-the-box reports&mdash;Customer Service historical analytics, Omnichannel historical analytics, Omnichannel real-time analytics, and knowledge analytics reports.

## Prerequisites

Grant **Create**, **Read**, **Write**, and **Delete** privileges to applicable security roles for the **Report Bookmark** custom entity. [Configure user access to analytics and dashboards](../administer/configure-customer-service-analytics-insights-csh.md#configure-user-access-to-analytics-and-dashboards).

## Create bookmarks

[!INCLUDE [Lightbox tip](../../../shared-content/shared/lightbox-tip.md)]

1. In Customer Service workspace or Contact Center workspace, open one of the following reports, **Customer Service historical analytics**, **Omnichannel historical analytics**, **Omnichannel real-time analytics**, or **Knowledge analytics**.

1. On the report page, select a tab, such as **Queue**.

1. Use the report filters to customize the data in your view.

1. Select **Bookmarks**, and then select **Create new**.

1. Enter a name for the bookmark, and then save it.

    :::image type="content" source="../media/manage-bookmarks.png" alt-text="Screenshot of creating a report bookmark to save personalized filters." lightbox="../media/manage-bookmarks.png":::

## Manage bookmarks

Select **Bookmarks**, and then on the **Bookmarks** menu:

- To delete a bookmark, select the delete icon.
- To set a bookmark as the default view for the report, select the pin icon. The report always opens to the pinned view.
- To reset the bookmarked view of a report, select **Reset**.

To modify a saved view, adjust the report filters as needed. Then select **Bookmarks** > **Update Bookmark**.

### Related information

[Customer Service dashboards](customer-service-analytics-insights-csh.md)  
[Omnichannel for Customer Service dashboards](omnichannel-analytics-insights.md)  
[Knowledge analytics](knowledge-search-analytics-cs.md)  
