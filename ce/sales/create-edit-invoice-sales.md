---
title: Create and manage invoices
description: An invoice is an order that has been billed to the customer. You can either convert an order into an invoice or create an invoice separately.
ms.date: 07/29/2024
ms.topic: article
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
searchScope: 
  - D365-App-msdynce_saleshub
  - D365-App-msdynce_salespro
  - D365-Entity-salesorder
  - D365-Entity-invoice
  - D365-UI-*
  - Customer Engagement
  - Dynamics 365
  - Sales
---
# Create and manage invoices

When a customer places an order, you can create an invoice to bill them for the upcoming sale. Typically, you convert an order into an invoice; however, you can also create an invoice that does not originate from an order.  

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Enterprise, Dynamics 365 Sales Premium, or Dynamics 365 Sales Professional <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | Any primary sales role, such as salesperson or sales manager<br>  More information: [Primary sales roles](security-roles-for-sales.md#primary-sales-roles)|


<a name="bkmk1"></a>   

## Create an invoice from an order  

1. Select the site map ![Site Map icon.](media/site-map-icon.png "Site map icon"), and then select **Orders**. 
  
2. Select the order you want to create an invoice from.  
  
3. Select **Create Invoice** at the top of the screen.  

    > [!IMPORTANT]
    > If Dynamics 365 Sales is integrated with an external order processing application, you may see the **Submit Order** button instead of the **Create Invoice** button on the Order form command bar. This is because the integration allows an order created in Dynamics 365 Sales to be submitted, after which it is synchronized with the order processing app where the lifecycle of the order continues. A submitted order is locked for editing in Dynamics 365 Sales, except by an integration user. [!INCLUDE[proc-more-information](../includes/proc-more-information.md)] [Enable sales order processing integration](developer/enable-sales-order-processing-integration.md)

4. Review the contents of the invoice and make any additions or corrections before sending to your customer.  

> [!NOTE]
> Your base record and all its line items must use the same currency. For example, if your invoice has the currency set to U.S. Dollars, you must use the same currency for the price list items that you add to the invoice. You can't change the currency of the base record (in this case, an invoice), unless you remove all the line items associated with the record.
> Similarly, if the invoice is created from an order that's created from a quote created from an opportunity, it must use the same currency as the opportunity.
  
## Create an invoice  
  
1. Select the site map ![Site Map icon.](media/site-map-icon.png "Site map icon"), and then select **Invoices**. 
  
2.  Select **New**.

3. On the **Invoice** form, enter data in the following required fields:

    -  **Name** 
  
    -  **Price List** and **Currency**: Select the price list and the currency that will be used to calculate the product prices. 

        > [!NOTE]
        > By default, selecting a price list is required to be able to add products to an invoice; however, your administrator can change your organization settings to make the Price List field optional. 

   -  **Prices Locked**. This field is read-only. You set **Prices Locked** by selecting **Lock Pricing** on the command bar. More information: [Lock or unlock the price for an order or invoice](lock-unlock-price-order-invoice.md), [Sales transactions in Dynamics 365 Sales](sales-transactions.md) 

4. In the **Sales Information** section, in **Potential Customer**, select the customer you're creating this invoice for.
  
5. On the command bar, select **Save** to create the invoice record.  
  
6. To add products from your opportunity to your invoice, select the **More options** icon ![More commands icon](media/more-commands-button.png "More commands icon") and then choose **Get Products**, select your opportunity, and select **OK**.  
  
    -OR-
    To manually add other products, in the **Products** section, select **Add Product**. For more information, see [Add products to Quote, invoice, or order records](add-product-quote-order-invoice.md). If your administrator has configured the enhanced experience for adding products, you'll see the **Add Products** button. For more information about adding products using the enhanced experience, see [Find and add multiple products to quotes, orders, or invoices](add-products-qoi-enhanced.md). 
    
    You need to enter the tax amount when you add a product to a quote, order, or invoice. Dynamics 365 Sales doesn't automatically calculate tax for individual products. However, the total tax is calculated automatically based on the sum of the tax amounts for all of the individual products in a quote, order, or invoice.  


8.  Select **Save and Close**.
  
## Close an invoice

You close an invoice either by canceling the invoice or setting the invoice status as paid. To do this, open the invoice you want to close, and on the command bar, select **Cancel Invoice** or **Invoice Paid**.

## Email an invoice

When you’ve added all the details to the invoice, you can directly email the invoice to the customer.

1. Open the invoice.
1. On the command bar, select the **More commands** icon ![More commands icon.](media/more-commands-icon.png "More commands icon"), select **Send by Email**.
    The email is ready to be sent with the invoice attached as a word document. 

## Typical next steps  

 ![Right arrow button](media/orange-right-arrow-button.png "Right arrow button") [Close an opportunity as won or lost (Sales)](close-opportunity-won-lost-sales.md)  
  
 ![Home button](media/home-button.png "Home button") [Learn about the sales process, nurturing sales from lead to order](nurture-sales-from-lead-order-sales.md)  
  
[!INCLUDE [cant-find-option](../includes/cant-find-option.md)]

## Related information  

[Nurture sales from lead to order](nurture-sales-from-lead-order-sales.md)  
[Print quote, invoice, or other records](print-records.md)   
[Troubleshoot issues with orders](/troubleshoot/dynamics-365/sales/troubleshoot-orders-issues)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
