---
title: Set default price level for opportunity, quote, order, and invoice (Dynamics 365 Sales)
description: Automatically set a default price level (price list) for an opportunity, quote, order, or invoice based on the sales territory of the user who creates or updates that table.
ms.date: 03/01/2023
ms.topic: article
applies_to: 
  - Dynamics 365 Sales
author: udaykirang
ms.author: udag
ms.reviewer: udag
search.audienceType: 
  - developer

---
# Set default price level for opportunity, quote, order, and invoice

You can automatically set a default price level (price list) for an opportunity, quote, order, or invoice based on the sales territory of the user who creates or updates the opportunity, quote, order, or invoice row.  
  
<a name="Enable"></a>   
## Enable automatic selection of default price level  
 To enable selection of default price level for opportunities, quotes, orders, or invoices based on the sales territory relationship, the following conditions must be true:  
  
- The value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` column is set to 1 (true). By default, the value is set to 1 (true).  
  
   You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_dynamics-365](../../includes/pn-dynamics-365.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether the default price level should be automatically selected for opportunities. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Configure product catalog information](/previous-versions/dynamicscrm-2016/administering-dynamics-365/dn832125(v=crm.8))  
  
- A price level is associated with a territory using the **Territory Default Pricelist** connection role, and the territory is assigned to the user who creates or updates the opportunity, quote, order, or invoice row.  
  
- The user has permission on the price level that is associated with the territory by using the **Territory Default Pricelist** connection role.  
  
  Dynamics 365 internally uses the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to determine the default price level for an opportunity, quote, order, or invoice based on the current user and the territory relationship with the price level. This is how the price level is set:  
  
- If a single price level is returned, the price level is automatically set for the opportunity, quote, order, or invoice row that the user is creating or updating.  
  
- If multiple price levels are returned, the price level field isn’t populated and the user must specify a price level for the opportunity, quote, order, or invoice row.  
  
<a name="Disable"></a>   
## Disable automatic selection of default price level  
 You can turn off the automatic selection of a default price level for your opportunity, quote, order, or invoice by setting the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` column to 0 (`false`), or by using the **Sales** tab in the system settings area in Dynamics 365 or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Configure product catalog information](/previous-versions/dynamicscrm-2016/administering-dynamics-365/dn832125(v=crm.8))  
  
<a name="Extend"></a>   
## Extend default price level selection  
 Instead of using the out-of-box rule for the selection of default price level for an opportunity, quote, order, and invoice, you can use the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to specify your custom logic for selecting default price level.  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_2015_update_1_admins](../../includes/cc-feature-included-with-2015-update-1-admins.md)]  
  
 To extend the default price level selection:  
  
1. Ensure that the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` column is set to 1 (true).  
  
2. Create a plug-in that contains custom code for returning price levels based on your business requirement.  
  
3. Register the plug-in on the `GetDefaultPriceLevel` message.  
  
   When you register a plug-in on the `GetDefaultPriceLevel` message, every time you create an opportunity, quote, order, or invoice row in [!INCLUDE[pn_dynamics-365.md](../../includes/pn-dynamics-365.md)], the plug-in is executed to return the price level based on your custom code.  
  
-   If a single price level is returned as a result of the plug-in execution, the price level is set for the opportunity, quote, order, or invoice row that the user is creating.  
  
-   If multiple price levels are returned as a result of the plug-in execution, the price level field is not populated and the user specifies a price level for the opportunity, quote, order, or invoice row.  
  
> [!NOTE]
>  When you extend the default price level selection by registering a plug-in on the `GetDefaultPriceLevel` message, the out-of-box selection of price level is disabled.  
  
## Related information  
 [PriceLevel table](entities/pricelevel.md)  
 <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest>  
 [Territory table](/power-apps/developer/data-platform/reference/entities/territory) 
 [Opportunity tables](opportunity-entities.md)  
 [Quote, order, and invoice tables](quote-order-invoice-entities.md)  
 [Write a plug-in](/powerapps/developer/common-data-service/write-plug-in)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
