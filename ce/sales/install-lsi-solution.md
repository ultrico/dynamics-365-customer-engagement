---
title: "Install the LinkedIn Sales Insights solution for accounts"
description: "Install the LinkedIn Sales Insights solution for accounts in Dynamics 365 Sales."
ms.date: 10/26/2021
ms.topic: article
author: udaykirang
ms.author: udag
ms.reviewer: udag
ms.custom: 
  - dyn365-sales
---
# Install LinkedIn Sales Insights 

Import the latest company profile data&mdash;such as personas, number of employees, and company URL&mdash;from LinkedIn Sales Insights into a matched account in Dynamics 365 automatically. Importing this data reduces the manual effort required to match company profiles between the two products, enter the details in Dynamics 365 Sales and frequently update data as LSI updates them.


## License and role requirements
| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium or Dynamics 365 Sales Enterprise  <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | System Administrator <br> More information: [Predefined security roles for Sales](security-roles-for-sales.md)|


## How LinkedIn Sales Insights helps

As an administrator, you can install LinkedIn Sales Insights and make it available for your sales teams to use. When installed, all the accounts that are available in your organization will display the **LinkedIn Sales Insights** tab in **Account** forms. Those accounts that have a matching LinkedIn Sales Insights company profile will show data from LinkedIn Sales Insights.

> [!div class="mx-imgBorder"]
> ![LinkedIn Sales Insights tab in an account form.](media/lsi-tab-account.png "LinkedIn Sales Insights tab in an account form")

## Review the prerequisites

Before you install LinkedIn Sales Insights, be sure you meet the following requirements:

- You have a **System Administrator** security role in Dynamics 365.
- You have a [Microsoft Relationship Sales](https://dynamics.microsoft.com/sales/relationship-sales/) subscription for Dynamics 365 and have signed up for [LinkedIn Sales Insights](https://business.linkedin.com/sales-solutions).    
    or     
    You've **LinkedIn Sales Navigator Team** or **LinkedIn Sales Navigator Enterprise** license, and have signed up your team for **LinkedIn Sales Insights**. More information: [LinkedIn Sales Solutions](https://business.linkedin.com/sales-solutions)

    >[!NOTE]
    >We recommend having a Microsoft Relationship Sales solution Plus license. To learn more, see the Dynamics 365 Sales section in the [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

- You've enabled JavaScript in your browser.
- You've disabled your pop-up blocker for the Dynamics 365 domain.
- CRM sync is enabled for your organization. More information: [Enable Sales Navigator CRM Sync & Activity Writeback for Dynamics 365](https://business.linkedin.com/sales-solutions/sales-navigator-customer-hub/resources/ms-dynamics-sync-activity-writeback)

## Install the solution

1. Go to the [LinkedIn Sales Insights for Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2154471) page, and then select **Get it now**.

    > [!div class="mx-imgBorder"]
    > ![LinkedIn Sales Insights for Dynamics 365 AppSource page.](media/lsi-appsource-page.png "LinkedIn Sales Insights for Dynamics 365 AppSource page")

2. Read the terms and conditions, and then select **Continue**.     

    > [!div class="mx-imgBorder"]
    > ![Select Continue to proceed with installation.](media/lsi-installation-continue.png "Select Continue to proceed with installation")

    A Power Platform admin center page opens where you can select the organization to install LinkedIn Sales Insights for Dynamics 365.

    > [!div class="mx-imgBorder"]
    > ![Select your organization to install LinkedIn Sales Insights.](media/lsi-select-organization.png "Select your organization to install LinkedIn Sales Insights")

3. In the **Select an environment** list, select your organization, select the check boxes for Microsoft and Dynamics 365 legal terms and privacy statements, and then select **Install**. On the **Manage your solutions** page, you can see the status of the installation.

To verify that the installation is complete, perform the steps in the following procedure.

## Validate the installation

1. In your app, select **Settings**, and then select **Advanced Settings**.
   > [!NOTE]
   > The **Advanced Settings** page is moving from the web client to an Unified Interface app. If your organization has enabled the public preview of the **Advanced settings redirection** feature, you’ll see the settings open in the Power Platform Environment Settings app. Find more information about the app and navigation path in [Advanced settings in the new experience](advanced-settings-new-experience.md).

2. Go to **Settings** > **Customizations** > **Solutions**.

3. Verify that the **msdyn_linkedinsalesinsights** solution is installed in your organization.

    > [!div class="mx-imgBorder"]
    > ![Validate the LinkedIn Sales Insights solution installation.](media/lsi-validate-installation.png "Validate the LinkedIn Sales Insights solution installation")

## Uninstall the solution

1. In your app, select **Settings**, and then select **Advanced Settings**.
   > [!NOTE]
   > The **Advanced Settings** page is moving from the web client to an Unified Interface app. If your organization has enabled the public preview of the **Advanced settings redirection** feature, you’ll see the settings open in the Power Platform Environment Settings app. Find more information about the app and navigation path in [Advanced settings in the new experience](advanced-settings-new-experience.md).

2. Go to **Settings** > **Customizations** > **Solutions**.

3. Select the **msdyn_linkedinsalesinsights** solution, and then select **Delete**.

4. In the confirmation message that appears, select **OK**.

The solution is removed from your organization.

[!INCLUDE [cant-find-option](../includes/cant-find-option.md)]

## Related information

[Understand the LinkedIn Sales Insights tab](understand-lsi-accounts-form.md)  
[LinkedIn Sales Insights for Dynamics 365 Sales - Installation Guide](https://www.linkedin.com/help/sales-navigator/answer/a419445)

