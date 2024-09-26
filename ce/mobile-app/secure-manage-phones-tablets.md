---
title: "Manage Dynamics 365 apps on mobile devices with Microsoft Intune | MicrosoftDocs"
ms.custom:
description: Secure and manage Dynamics 365 for phones and tablets using Microsoft Intune.
ms.date: 09/27/2021
ms.reviewer:
ms.service: d365ce-op
ms.topic: article
applies_to: Dynamics 365 apps
ms.assetid: 59af6fe5-f6e0-43d0-addc-044009bc0a23
caps.latest.revision: 24
ms.author: sericks
author: sericks007
search.audienceType:
  - admin
  - customizer
  - enduser
---
# Manage Dynamics 365 apps on mobile devices with Microsoft Intune  

If your organization is set up with Intune, you can use it to manage the Dynamics 365 for phones and tablets apps on Apple, Android, and Windows 10 tablets. Intune manages encryption at the device level, as well as app-to-app communications. With Intune, you can selectively wipe managed apps and related data on devices that are unenrolled, no longer compliant, lost, stolen, or retired from use.

With CRM Online 2016 Update 1 and later, you can use Intune mobile application management (MAM) without enrolling the device. This protects company data in Dynamics 365 apps without requiring you to enroll and deeply manage the end user's entire device. This is particularly useful for bring-your-own-device (BYOD) scenarios where end users don’t want to or can’t enroll their devices for IT management. This capability is also useful if a device is already enrolled in another mobile application management solution.

For more information about getting and using Intune, see [Microsoft Intune](/intune/fundamentals/what-is-intune) 

> [!NOTE]
> Managed app configuration solutions aren't supported so admins can't configure apps to start or run with specific settings enabled.   
  
  
## Set up conditional access to Dynamics 365 apps  
You can use the Azure portal to administer conditional access to manage access to Dynamics 365 apps from mobile devices based on conditions you specify. 

For more information about setting up conditional access on the Power Platform side, see [Azure AD Conditional Access](/power-platform/admin/restrict-access-online-trusted-ip-rules). 

For more information on conditional access, see [Conditional Access: Conditions](/azure/active-directory/conditional-access/technical-reference).

It's important to note that Intune cache conditional access policies can take up to 24 hours to propagate. If you don't want to wait then you can uninstall and then reinstall the app.
  
> [!NOTE]
>  To use conditional access, you must have an Azure Active Directory premium subscription.

  
### See also

[Dynamics 365 for phones and tablets User's Guide](../customerengagement/on-premises/basics/dynamics-365-phones-tablets-users-guide-onprem.md)  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
