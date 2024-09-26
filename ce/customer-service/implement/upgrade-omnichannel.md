---
title: "Upgrade Omnichannel for Customer Service | MicrosoftDocs"
description: "Perform the steps mentioned in the topic to upgrade to the latest version of Omnichannel for Customer Service."
author: neeranelli
ms.author: nenellim
ms.topic: article
ms.date: 03/12/2024
---

# Upgrade Omnichannel for Customer Service

[!INCLUDE[cc-use-with-omnichannel](../../includes/cc-use-with-omnichannel.md)]

Upgrade to the latest version of Omnichannel for Customer Service to unlock the benefits of new features. You can now upgrade to the latest release of Omnichannel for Customer Service from the **Omnichannel environments** page in **Dynamics 365 Admin Center**.

See [What's new in Omnichannel for Customer Service](../omnichannel-whats-new.md) to learn about the new features in the latest release.

Do the following steps to upgrade Omnichannel for Customer Service:

> [!NOTE]
> You'll be able to use the [admin center experience](/dynamics365/contact-center/implement/provision-channels#set-up-channels) to provision channels in your environment after it's available in your region. Once the new experience is available, you can only view existing environments and channels in the Power Platform admin center.

1. Log in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
2. Expand **Resources**, and select **Dynamics 365 apps**.
3. On the **Dynamics 365 apps** page, scroll to the **Omnichannel for Customer Service** application, select the ellipses (**...**), and then select **Manage**. The **Omnichannel environments** page opens on a new tab.
4. Select your environment under **Manage environments** in the left pane.
5. Select the **Upgrade** button that is enabled when an upgrade is available. 

    The system begins the upgrade and displays the message **Omnichannel upgrade is currently in progress**.
     
    When the upgrade process is completed successfully, your environment is upgraded to the latest version, and the message **Omnichannel for Customer Service upgrade was completed successfully** is displayed with the date.

   > [!div class=mx-imgBorder] 
   > ![Upgrade complete.](../media/upgrade-complete.png)

## Upgrade Omnichannel for Customer Service package on Unified Service Desk

If you are using Omnichannel for Customer Service on Unified Service Desk, see [Deploy package on Dynamics 365 Customer Service instance](../../unified-service-desk/oc-usd/omnichannel-customer-service-package.md#deploy-package-on-dynamics-365-customer-service-app) to upgrade.

### Related information

[Omnichannel for Customer Service system requirements](system-requirements-omnichannel.md)  
[Provision channels](/dynamics365/contact-center/implement/provision-channels#set-up-channels)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
