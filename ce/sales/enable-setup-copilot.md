---
title: Turn on and set up Copilot in Dynamics 365 Sales
description: Learn how to turn on and set up Copilot in Dynamics 365 Sales to improve sales productivity and effectiveness. 
ms.date: 07/31/2024
ms.topic: how-to
ms.service: dynamics-365-sales
search.app: salescopilot-docs
ms.collection: bap-ai-copilot
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
ms.custom:
  - bap-template
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/03/2023
---

# Turn on and set up Copilot in Dynamics 365 Sales

Effective April 1, 2024, Copilot in Dynamics 365 Sales is turned on by default for the following orgs:

- Orgs in [regions where an Open AI Service endpoint is available](/power-platform/admin/geographical-availability-copilot#regions-involved-with-copilots-and-generative-ai-features). 
- Orgs that have [provided consent for data movement across regions](/power-platform/admin/geographical-availability-copilot#regions-involved-with-copilots-and-generative-ai-features).

For all the other orgs, an admin must provide consent in the Power Platform admin center and then turn on Copilot in the Sales Hub app. This article provides instructions for turning Copilot on or off, providing consent for data movement, and configuring Copilot for your business.

> [!IMPORTANT]
>- If you had previously turned Copilot off, it remains turned off. 
>- Throughout this article, the term sales apps refers to apps that have lead and opportunity tables and are not part of the [exclusion list](sales-copilot-faq.md#which-applications-are-in-the-exclusion-list-for-copilot-in-dynamics-365-sales).

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | [Dynamics 365 Sales Premium or Dynamics 365 Sales Enterprise](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | [System Administrator](security-roles-for-sales.md) |

For more information about the licensing requirements for Copilot in Dynamics 365 Sales, see [licensing FAQs](/power-platform/admin/powerapps-flow-licensing-faq#licensing-for-copilot-chat-and-form-fill-assistance-in-model-driven-apps)

## Prerequisites

- Verify whether your org is in a region where Copilot in Dynamics 365 Sales is available. For a list of regions where Copilot is available, see the [Copilot international availability report](https://releaseplans.microsoft.com/availability-reports/?report=copilotproductreport).
- Verify whether your region has an Azure OpenAI Service endpoint. If not, you must provide consent for data movement across regions to use Copilot in Dynamics 365 Sales. For more information, see [Copilot data movement](sales-copilot-data-movement.md).

## Turn Copilot features on or off in Sales Hub

1. In the Sales Hub app, go to **Change area** in the lower-left corner of the page and select **App Settings**.

1. Under **General Settings**, select **Copilot**.

1. In the **Set up Copilot in Dynamics 365 Sales** page, select **Try our newest preview features before they're rolled out to everyone** to get all the Copilot preview features automatically.

1. If your org is in a region where Azure Open AI Service endpoint isn't available but you didn't provide the consent for data movement, select **Go to Power Platform admin center** and follow the [instructions to provide consent](/power-platform/admin/geographical-availability-copilot#turn-on-copilots-and-generative-ai-features-1).

1. Under **All Dynamics 365 Sales apps**, select a global setting that you want to apply to all Sales apps and then override the setting at the app-level. For example, if you want to enable Copilot only for the Sales Hub app, select **Off** for **All Dynamics 365 Sales apps** and then select **On** only for the Sales Hub app.  

    :::image type="content" source="media/enable-copilot.svg" alt-text="Screenshot of the new settings page in Dynamics 365 Sales Hub." lightbox="media/enable-copilot.svg":::  

    The initial setting on the **Set up Copilot in Dynamics 365 Sales** page depends on the setting for the org and the app. For example, if your Power Platform admin turned Copilot on for your org but your Power Apps admin turned it off for the Sales Hub app, the initial setting in the **Set up Copilot in Dynamics 365 Sales** page is set to **Off** for Sales Hub app and **On** for all other Sales apps. 

    <a name="default-setting-copilot"></a>

    The **Default** setting has the following behavior:
    
    - For orgs in North America, Copilot Chat is turned on for all Dynamics 365 Sales apps (with lead and opportunity tables). Copilot for email is turned on only if you had opted in for early access.

    - For orgs in other regions, Copilot is turned on for all Dynamics 365 Sales apps that meet the following conditions:

        - Consent for data movement is provided for the org.

        - The [release channel](/power-apps/maker/model-driven-apps/channel-change) for the app is set to **Monthly release channel**.

        - For Copilot for email, you had [opted in for preview features](copilot-preview-features.md).
    
    - For apps that don't meet the above conditions, the **Default** setting turns Copilot off.

1. Select **Turn audit on** to turn on audit history for the lead and opportunity tables. If auditing is already turned on for the lead and opportunity tables or globally, the **Turn audit on** option isn't displayed.

    - Audit history is required for Copilot to display recent changes to leads and opportunities.
    - If you configure Copilot to [show recent changes from tables other than leads and opportunities](copilot-configure-summary-fields.md), turning on auditing turns on audit history for those tables as well. However, if you remove those fields later, you need to [turn off audit history](/power-platform/admin/manage-dataverse-auditing#enable-or-disable-auditing-for-an-entity) for those tables manually.

1. Select **Save**.

    The Welcome to Copilot pane opens in the right side pane with a quick tour.

## Add the Copilot page site map entry to custom sales app

When you create a custom model-driven app, you can choose a default solution to create a site map for it. However, you can choose solutions that are based on table forms only. The full-screen Copilot page is based on a URL custom control and doesn't appear in the list of solutions. You must add it to the site map manually.  

Add the Copilot page to your site map by following the instructions in [add site map entry to your custom app](add-custom-site-map.md) and enter or paste the following URL:

`/main.aspx?&pagetype=control&controlName=PowerApps.Copilot`

## Add the opportunity summary widget to custom forms

To add the opportunity summary widget to custom forms, follow these steps:

1. Sign in to the [Power Apps maker portal](https://make.powerapps.com).
1. From the site map, select **Tables** and open the table.
1. From the Data experience section, select **Forms**.
1. Open your custom form for which you want to add the opportunity summary widget.
1. On the command bar, select **Component** and then add the **1-column section** component to the form as a placeholder for the widget.
1. From the **Component** site map, select Display and then add the **Record summary** to the newly added column.  

    The opportunity summary widget is added to the form.

    >[!NOTE]
    >To hide the **New section** label, go to the **Properties** tab of the **New Section** settings pane, and then select **Hide label**.  

1. Save and publish the form.

## Next steps

- [Configure fields for generating summaries and recent changes list](copilot-configure-summary-fields.md)
- [Configure fields for generating what's new with my sales records list](copilot-configure-whatsnew-field.md)
- [Configure Copilot to use specific SharePoint locations](copilot-sharepoint-config.md)


## Related information

- [Use Copilot in Dynamics 365 Sales](use-sales-copilot.md)
- [Copilot data movement](sales-copilot-data-movement.md)  
- [FAQs about Copilot in Dynamics 365 Sales](sales-copilot-faq.md)
