---
title: Scan business cards in Dynamics 365 Sales
description: Use the business card scanner in Dynamics 365 Sales to quickly scan business cards of the prospective customers you've met with.
ms.date: 02/02/2024
ms.topic: how-to
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
ms.custom: bap-template
searchScope: 
  - D365-App-msdynce_saleshub
  - D365-App-msdynce_salespro
  - D365-Entity-contact
  - D365-UI-*
  - Dynamics 365
  - Sales
  - Customer Engagement
---
# Scan business cards in Dynamics 365 Sales

The integrated business card scanner in Dynamics 365 Sales helps salespeople to quickly scan business cards of the prospective customers they’ve met in the fields. It reads basic information from the card and populates data in fields of **lead** or **contact** records in Dynamics 365 Sales, so salespeople don’t spend time on entering the data manually and can focus on more important tasks.

> [!IMPORTANT]
> - To learn about the availability of the business card feature in a region, see [Feature availability by region](/ai-builder/availability-region#availability-and-release-status-of-features-by-region).
> - Ensure that your security role has read permissions for the **msdyn_AIModel** and **msdyn_AITemplate** tables. To get permissions, contact your system administrator. More information: [Security roles and privileges](/power-platform/admin/security-roles-privileges)
> - To know about the business card scan limits with your user license, see the [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/p/?LinkId=866544).
> - The card scanner is available in lead and contact forms. If you'd like to add the card scanner to other forms, see [Use the business card reader component in model-driven apps in Power Apps](/ai-builder/business-card-reader-component-model-driven)

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium or Dynamics 365 Sales Enterprise. <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | Basic User in Power Platform <br> More information: [Assign security roles to users in a Dataverse environment](/power-platform/admin/database-security#assign-security-roles-to-users-in-an-environment-that-has-a-dataverse-database) <br> [Assign security roles to users in non-Dataverse environment](/power-platform/admin/database-security#assign-security-roles-to-users-in-an-environment-that-has-no-dataverse-database)  |
|||

## Scan a business card

1. On the nav bar, select the **New** button and then select **Contact** or **Lead**.  

    :::image type="content" source="media/nav-bar.png" alt-text="Navigation bar highlighting the Quick Create button":::


2.  On the Quick Create form, select **Scan Business Card**.

    > [!div class="mx-imgBorder"]
    > ![Option to scan business card in the Contact Quick Create form.](media/scan-business-card-option-in-contact-quick-create-form.png "Option to scan business card in the Contact Quick Create form")

3.  If you’re using the Dynamics 365 Sales app on a desktop, browse to the folder where the business card picture is stored, select the business card picture, and then select **Insert**.

    -OR-

    If you are using a mobile phone, use the mobile phone camera to capture the business card picture.

    The details like first name, last name, job title, and email will be automatically populated from the business card. Account name is not populated automatically as it's a lookup field. You can select it manually in the **Account Name** field.

    > [!div class="mx-imgBorder"]
    > ![Contact form showing scanned card with automatically populated fields.](media/scanned-card-with-populated-fields.jpg "Contact form showing scanned card with automatically populated fields")

4. Select **Save**.

    > [!NOTE]
    > - When you save the **Contact** or **Lead** records, a **Duplicate Records detected** dialog box is shown if duplicate records are found based on the available duplicate detection rules. You can choose whether you want to create a duplicate record or not.  
    > - When you save the **Contact** or **Lead** record, the business card is also associated and stored in the records, so you can refer to it later. If your system administrator has set the **Always retain business card images after scanning option** option to **No**, the business card image won't be saved. 

    > [!div class="mx-imgBorder"]
    > ![Saved business card on the Business card tab of a Contact form.](media/saved-business-card-on-business-card-tab.jpg "Saved business card on the Business card tab of a Contact form")

[!INCLUDE [cant-find-option](../includes/cant-find-option.md)]

## Related information

[Customize the business card scanner control](customize-business-card-scan-control.md)  
[Enable or disable saving of business card image](retain-business-card-image-after-scanning.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
