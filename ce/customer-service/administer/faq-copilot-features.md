---
title: FAQ for copilot features
description: FAQ for copilot features in Dynamics 365 Customer Service.
ms.date: 05/14/2024
ms.topic: article
author: gandhamm
ms.author: mgandham
search.audienceType: 
  - admin
ms.custom: 
  - dyn365-customerservice
ms.collection: bap-ai-copilot
---


# FAQ for Copilot in Customer Service

This FAQ article helps answer the questions around the Copilot features in Customer Service.

## In which Customer Service apps is Copilot available?  

Copilot is available in Customer Service workspace, Customer Service Hub, and [custom apps](../administer/copilot-powerapps-settings.md). 

## Which are the copilot features available across apps?

The following table describes the availability of Copilot features across apps.

| Feature name | Customer Service workspace | Customer Service Hub | Custom apps |
| ------- | ----- | -------- | ----- | 
| Copilot knowledge chat| ✔ | O | O |
| Copilot for drafting emails| ✔ | O  |O  |
| Case summarization| ✔ | O  | O  |
| Copilot analytics| ✔ | O | O |
| Conversation summarization| ✔ | ✖ | ✖ |


✔ : Available out of the box 
O  : Available, but configuration is required in Power Apps 
✖ : Not available 

## Why does Copilot come back with a different response to the same exact input? 

Copilot's response to the same question can vary due to multiple factors. Copilot is built on a generative AI language models. While measures are in place to minimize response variability, there's a possibility that Copilot might generate slightly different answers. Additionally, in multiturn questions, Copilot considers the previous question's context as input. Therefore, asking Copilot the same question at the start of the session versus in the middle can result in different responses.

## Can Copilot read tables and images in my knowledge articles?
 At this time, Copilot cannot read tables and images in knowledge articles. 

## What are the limitations for webpages as sources? 

You can add up to five trusted domains as web sources, and the domains must be publicly indexed by Bing search. 

## Does Copilot support knowledge articles published in all languages? 

Yes. Copilot supports knowledge articles published in the supported languages. See: 
[Language support for AI-based analytics and insights in Customer Service](cs-region-availability-service-limits.md#language-support-for-ai-based-analytics-and-insights-in-customer-service)

## What are the best practices for configuring copilot?
 
- Make sure that you use high-quality knowledge sources for copilot to generate responses from.
- Revisit your copilot knowledge sources before you enable Copilot.
- Restrict access to sources from which you don't want your copilot responses to be generated.

### Related information

[Responsible AI FAQ for Copilot in Customer Service](../implement/faq-responsible-ai-copilot.md)  
[FAQ for Copilot data security and privacy in Microsoft Power Platform](/power-platform/faqs-copilot-data-security-privacy)  