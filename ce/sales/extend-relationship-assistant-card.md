---
title: Create custom cards in Assistant
description: Use the assistant to create custom cards that help in displaying insight cards that are specific to your organization.
ms.date: 09/20/2024
ms.topic: how-to
author: udaykirang
ms.author: udag
ms.reviewer: udag
---

# Create custom cards in Assistant  

Use the assistant to create custom action cards that help in displaying insight cards that are specific to your organization.

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | System Administrator or System Customizer <br>  More information: [Predefined security roles for Sales](security-roles-for-sales.md)|

## What are actions or insight cards?

Action cards provide you up to date information on email, meeting, and more in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]. These cards remind you of upcoming activities; it evaluates your communications, and suggests when it might be time to reach out to a contact that’s been inactive for a while; it identifies email messages that may be waiting for a reply from you; it alerts you when an opportunity is nearing its close date; and much more. These cards are displayed on forms, dashboards, and throughout the application to provide relevant information for the context you're working in at the moment.  
[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action cards reference](action-cards-reference.md)  

The action cards contain the following basic elements:  
:::image type="content" source="media/card-type-dev.png" alt-text="Screen shot of action cards basic elements.":::

1. **Generics actions:** The more options consist of the following actionable buttons:  
    - **Snooze button:** Hides card temporarily. Snooze time varies by card type. Once the snooze time expires the card will again be visible.  
    - **Dismiss button:** Dismisses card permanently, regardless of whether you have completed the action.  
1. **Actions area:** Provides convenient links that help you complete whatever type of action the card is recommending. The number (up to two) and types of links provided here vary by card type.  
1. **Main content area:** Shows the title of the record the card refers to, its summary, the card type, and other basic information. Select anywhere in this area (except for on the two buttons) to open the related item, which might be a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] record or an email message.

## Create a custom card

You can generate these custom cards in two ways:  

- As a sales manager or administrator, you can generate custom insight cards (known as action cards) by using the **Assistant** which is based on Microsoft Flow. This provides you with a graphical user interface to generate custom cards. To learn more, see [Preview: Manage insight cards](manage-custom-cards-flow.md).  
    >[!NOTE]
    > We recommend you to use the **Assistant** to generate the custom insight cards.  
- As a developer, you can create card types according to your organizational requirements and make them available for users. To learn more, see [Sample: Create custom insight cards type](sample-extend-relationship-assistant-card-type.md)  
    >[!NOTE]
    >To use this feature, you must purchase a **Dynamics 365 Sales Insights** license, or start a trial to use Sales Insights features.

[!INCLUDE [cant-find-option](../includes/cant-find-option.md)]

## Related information

[Manage insight cards](manage-custom-cards-flow.md)  
[Sample: Extend assistant card type (custom card)](sample-extend-relationship-assistant-card-type.md)  
[Configure Assistant](configure-assistant.md)  
[Guide customer communications with assistant](assistant.md)
