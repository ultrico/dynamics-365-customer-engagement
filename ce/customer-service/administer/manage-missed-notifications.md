---
title: Enable missed notifications
description: Learn about managing notifications that are missed by agents.
ms.date: 06/14/2024
ms.topic: how-to
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.collection:
ms.custom: bap-template
---

# Enable missed notifications

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability-embedded-yes.md)]

With the missed notifications feature, you can choose to automatically set agent presence to inactive, so that no new tasks will be assigned when agents miss notifications for incoming chat requests. In addition to the status change, a message bar indicating that a notification has been missed will be displayed on the agent dashboard. Agents can reset their status by using the reset presence option that's displayed with the notification or by manually changing their status.

> [!IMPORTANT]
> 
> - Missed notifications won't work if **Away** is included as an allowed presence for work streams. More information: [Understand and create work streams](../work-streams-introduction.md)
> - Missed notifications is not supported in Omnichannel for Customer Service on Unified Service Desk.

## Enable automatic update of agent presence when a notification is missed

1. In the site map of Customer Service admin center or Contact Center admin center, select **Workspaces** in **Agent experience**, and then select **Notification templates**.

1. On the **Omnichannel Configuration** page, select the **Missed Notifications** tab.

1. Set the **Change agent status to inactive after a missed notification** toggle to **Yes**. The **Status name** and **Status description** settings appear.

1. Select **Save**.

> [!div class=mx-imgBorder] 
> ![Enable missed notifications.](../media/enable-missed-notifications.png "Enable missed notifications")

### Related information

[Manage notification settings and templates](/dynamics365/app-profile-manager/notification-templates)  
[View notifications](../use/oc-notifications.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
