---
title: Understand the sales pipeline chart and its phases
description: Understand how sales reps or managers use the Sales Pipeline chart to visualize revenue for an opportunity.
ms.date: 11/20/2023
ms.topic: conceptual
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
searchScope:
  - D365-App-msdynce_saleshub
  - D365-App-msdynce_salespro
  - D365-Entity-*
  - D365-UI-Dashboard
  - Dynamics 365
  - Sales
  - Customer Engagement
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/17/2023
  - bap-template
---
# Understand the sales pipeline chart and its phases 

Sales reps or managers use the out-of-the-box Sales Pipeline chart to visualize the revenue for an opportunity based on each pipeline phase. The following image shows a sample Sales Pipeline chart with pipeline phases such as 1-Qualify, 2-Develop, and so on. 

:::image type="content" source="media/sales-pipeline-chart.png" alt-text="Screenshot of the sales pipeline chart.":::

> [!NOTE]
> If you've associated different stages of the business process flow to multiple entities, the pipeline phases shown in the chart will only be based on the stages associated with the opportunity entity. For example, if you've associated only the qualify and develop stages with the opportunity entity, the chart displays data only for these two stages.

The pipeline phase of an opportunity is based on the stage of the business process flow that it's currently in. When an opportunity moves through the stages of its business process flow, the pipeline phase is set to a value in the form of _{StageCategoryIndex} - {CategoryName}_.

To understand how each of the pipeline phases is named, go to the **Settings** area for the opportunity and open the business process flow definition associated with the opportunity record. 
 
There are four stages in the out-of-the-box Opportunity Sales Process flow. Each stage is mapped to a unique category, as highlighted in the **Properties** section of the following image. You can customize the business process flow definition by adding or removing stages, and you can also change the name displayed for each stage. The value of the pipeline phase attribute is based on the category of the stage and isn't affected by any change you make to the display name. 

![Opportunity Sales Process definition.](media/opportunity-sales-process-definition.png "Opportunity Sales Process definition")
 
The category values used for each business process stage are defined in a global option set named **Stage Category**. When an opportunity moves from the **Qualify** to **Develop** stage of the Opportunity Sales Process flow, the metadata for the category of the new stage (**Develop**, in this example) is read. Because the order of the **Develop** stage in our example is **2**, the pipeline phase of the opportunity is set to **2-Develop**.

![Stage Category option set.](media/stage-category.png "Stage Category option set")

The label for the pipeline phase of an opportunity consists of the category order (index) of the associated stage followed by the name of the category. In this way, pipeline phases are arranged in a sequence that matches the order of the associated category options in the **Stage Category** option set metadata. If you have a business need to introduce a new stage in the flow&mdash;for example, you want the stage **Negotiation** to appear between the **Propose** and **Close** stages&mdash;you must add a new category option named **Negotiation** in the **Stage Category** option set, and ensure that it's positioned between **Propose** and **Close**, and select this new category option for the Negotiation  stage of the business process flow. 


## Related information

- [Manage opportunities using pipeline view](use-opportunity-pipeline-view.md)  
- [Gain insights with dashboards in Dynamics 365 Sales](dashboards.md)  
- [Troubleshooting sales pipeline chart and its phases](/troubleshoot/dynamics-365/sales/troubleshoot-sales-pipeline-issues)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
