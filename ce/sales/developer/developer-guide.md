---
title: Developer Guide
description: This guide contains entity reference and action reference information that developers need to know while developing for Dynamics 365 Sales.
ms.date: 05/01/2024
ms.topic: overview
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
---

# Developer Guide for Dynamics 365 Sales 

Welcome to the Dynamics 365 Sales Developer Guide. Use this guide to understand the tables (formerly known as entities) and actions that are available in Dynamics 365 Sales. 

As a developer or system customizer, you can [use the Dataverse WebAPI](/powerapps/developer/common-data-service/webapi/overview) to interact with these tables and actions. You can update values in the Sales tables, even if the fields or forms are marked as read-only in the user interface. However, you must be aware of the implications of changing these values. We recommend that you test your changes in a development environment before deploying them to a production environment.


[!INCLUDE[cc-app-definition-sales-dev](../../includes/cc-app-definition-sales-dev.md)]

<br />
<table>
<tr>

<td>
<h2>Model your business data</h2>
<li><a href="../developer/competitor-entity.md" data-raw-source="[Competitor entity](../developer/competitor-entity.md)">Competitor table</a></li>
<li><a href="../developer/lead-entity.md" data-raw-source="[Lead entity](../developer/lead-entity.md)">Lead entity</a></li>
<li><a href="../developer/opportunity-entities.md" data-raw-source="[Opportunity entity](../developer/opportunity-entities.md)">Opportunity entity</a></li>
<li><a href="../developer/quote-order-invoice-entities.md" data-raw-source="[Quote, order, and invoice entities](../developer/quote-order-invoice-entities.md)">Quote, order, and invoice tables</a></li>
<li><a href="../developer/marketing-entities-campaign-list.md" data-raw-source="[Marketing entities (campaign, list)](../developer/marketing-entities-campaign-list.md)">Marketing entities (campaign, list)</a></li>
<li><a href="../developer/goal-management-entities.md" data-raw-source="[Goal management entities](../developer/goal-management-entities.md)">Goal management tables</a></li>
<li><a href="../developer/product-catalog-entities.md" data-raw-source="[Product catalog entities](../developer/product-catalog-entities.md)">Product catalog tables</a></li>
<li><a href="../developer/sales-literature-entities.md" data-raw-source="[Sales literature entities](../developer/sales-literature-entities.md)">Sales literature tables</a></li>
</td>

<td>
<h2>Table reference</h2>

  <li><a href="../developer/entities/invoice.md" data-raw-source="[Invoice](../developer/entities/invoice.md)">Invoice</a></li>
  <li><a href="../developer/entities/lead.md" data-raw-source="[Lead](../developer/entities/lead.md)">Lead</a></li>
  <li><a href="../developer/entities/opportunity.md" data-raw-source="[Opportunity](../developer/entities/opportunity.md)">Opportunity</a></li>
  <li><a href="../developer/entities/product.md" data-raw-source="[Product](../developer/entities/product.md)">Product</a></li>
  <li><a href="../developer/entities/quote.md" data-raw-source="[Quote](../developer/entities/quote.md)">Quote</a></li>
  <li><a href="../developer/entities/salesorder.md" data-raw-source="[SalesOrder](../developer/entities/salesorder.md)">SalesOrder</a></li>

</td>
</tr>
<tr>
<td>
<h2>Sales Action Reference</h2>
  <li><a href="reference/custom-actions/msdyn_ForecastApi.md" data-raw-source="[msdyn_ForecastApi](reference/custom-actions/msdyn_ForecastApi.md)">msdyn_ForecastApi</a></li>
  <li><a href="reference/recalculateprice-action.md" data-raw-source="[RecalculatePrice Action](reference/recalculateprice-action.md)">RecalculatePrice Action</a></li>
</td>
<td>
<h2>Sales Premium</h2>
<li><a href="../developer/entities/msdyn-connectsequence-action.md" data-raw-source="[msdyn_ConnectSequence Action](../developer-sp/msdyn-connectsequence-action.md)">msdyn_ConnectSequence Action</a></li>
<li><a href="../entity-reference.md" data-raw-source="[Entity reference](../entity-reference.md)">Entity reference</a></li>

</td>
</tr>
</table>

### Related resources

[Overview of Sales and Sales Hub](../overview.md)<br />
[Help resources for seller in Dynamics 365 Sales](../user-guide.yml)  
[Administrator and Sales Manager Guide](../admin-guide.yml)<br />


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
