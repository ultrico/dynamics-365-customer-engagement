---
title: Relationship intelligence FAQs
description: Get answers to frequently asked questions about relationship analytics and health, and who knows whom.
ms.date: 03/15/2024
ms.topic: troubleshooting
author: udaykirang
ms.author: udag
ms.reviewer: udag
ms.owner: shujoshi
ms.custom:
  - bap-template
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/11/2024
---

# Relationship intelligence FAQs

This article answers frequently asked questions about relationship analytics and health, and who knows whom in Dynamics 365 Sales and Sales premium.

## Relationship analytics and health

### Which data is used to generate relationship insights?

**Basic insights:**

Uses email, phone call, and appointments sent or received in Dynamics 365.

**Enhanced insights:**

Uses email, phone call, and appointments sent or received in Dynamics 365 and Exchange (if configured).

### What is the frequency of KPI updates?

**Basic insights:** 

Updated in near real-time&mdash;as soon as a related activity is marked as completed in Dynamics 365.  

**Enhanced insights:**

Updated every 24 hours. ​  

### What are the signals in relationship health?
​
Relationship health looks at activity, recency, engagement, and sentiment of activities between sellers and customers.

### Is Office 365 consent mandatory for the relationship intelligence feature to work?
 
Office consent isn't mandatory for relationship analytics, health score, and who knows whom. You’ll get basic relationship insights based on the data in Dynamics 365. When you provide consent in Office 365 to use Exchange data, you’ll get more accurate and complete relationship information.

### What happens if I select the Exchange checkbox but the Office 365 admin hasn’t provided the consent?

The data from Exchange isn't collected until consent is provided. Work with your Office 365 administrator to [get consent to collect Office 365 data](provide-consent-office365.md).

### Why is the Exchange option selected although I didn't select it or provide the required consent?

The Exchange option in Relationship intelligence settings is selected by default in some cases. However, no data is collected from Exchange until your Office 365 administrator provides consent. You can clear the option if you aren't planning to integrate with Exchange.
  
### Can I influence the relationship health score?​

An administrator can influence the relationship health score by changing the weight of activity types and the expected level of communications with customers. More information: [Configure relationship analytics and health](configure-relationship-analytics.md)

### How are similar won deals identified? <a name="similar-won-deals-fields"></a> 
 
Dynamics 365 Sales uses AI models to determine the factors that affect the identification of similar won deals. The factors may differ from organization to organization based on custom and out-of-the-box fields.

To view the fields that determine the similar won deals at that point in time, select the information icon corresponding to any section heading and a side pane opens with the field information.

:::image type="content" source="media/faq-sa-about-relationship-analytics-side-pane-fields.png" alt-text="Screenshot of the relationship analytics side pane.":::

## Who knows whom

### Why am I not seeing some of my colleagues in the who knows whom suggestions?

If you know that a colleague has interacted with a customer but their information is not shown in Who Knows Whom widget, it could be due to the following reasons:

**Basic insights:** 

Displays the five colleagues who contacted the customer the most through emails and appointments in Dynamics 365. Colleagues who contacted the customer by phone and those who had fewer interactions through emails and appointments aren't listed.

**Enhanced insights:**

- Those colleagues aren't part of your Dynamics 365 org.
- Those colleagues aren't part of the security role that's [enabled for relationship intelligence](enable-ri.md).  
- Those colleagues are part of the security group that your Office 365 admin has [opted out](provide-consent-office365.md).
- Those colleagues have explicitly [opted out of sharing their data](who-knows-whom.md#turn-off-data-sharing-with-dynamics-365-applications).

[Which colleagues show up as connections?](#which-colleagues-show-up-as-connections)

### How long does it take for suggestions to appear?

**Basic insights:** Who knows whom suggestions are available out-of-the-box if the email and appointment data is available in Dynamics 365.

**Enhanced insights:** After your Microsoft 365 admin provides consent, you'll start seeing the results within a day. However, the suggestions may not be complete right away because the data is processed in batches over a period of four days.  

### Which colleagues show up as connections?

**Basic insights:** Colleagues who have contacted the customer the most through emails and appointments in Dynamics 365.

**Enhanced insights:** Users in your organization who have frequently and recently interacted with the contact or lead show up as connections, unless they have opted out. Administrators have the option to [opt out groups](provide-consent-office365.md) such as C-suite, M&A, finance, and so on. Users can opt out by [turning off data sharing with Dynamics 365 applications](who-knows-whom.md#turn-off-data-sharing-with-dynamics-365-applications).

### How are the connections weighted?

**Basic insights:** Uses only frequency. The connections are weighted based on the number of interactions through emails and appointments in Dynamics 365. Top five users who have interacted the most with the contact or lead are displayed.  

**Enhanced insights:** Uses frequency and recency. If your administrator has enabled Exchange integration, the connections are weighted based on recent and frequent interactions through emails or appointments. 

Every seller will see the same set of introducers for a contact or lead. 

### How frequently is the data collected?

**Basic insights:** Collected in near real-time&mdash;as soon as a related activity is marked as completed in Dynamics 365.  

**Enhanced insights:** When you enable who knows whom and provide the required consent, Exchange data for the last year is collected and insights are generated based on that data. After this, Exchange data is collected daily and insights are updated based on the latest data.  

### What is the source for who knows whom data?

**Basic insights:** Emails and appointments sent and received in Dynamics 365.

**Enhanced insights** Emails and meeting information in Exchange Online is the source data. [Learn more about how connections weighted](#how-are-the-connections-weighted)

### Where are the insights from Exchange generated?

After the Microsoft 365 admin provides consent, the Exchange data is collected and stored in Dynamics 365. Insights are generated from the stored data in Dynamics 365.  

> [!IMPORTANT]
> Microsoft 365 and Dynamics 365 each have their own service-specific licensing terms. The service-specific terms that apply depend on which service processes your data. For example, when a copy of your Microsoft 365 data is transferred to Dynamics 365, your Microsoft 365 data in that copy becomes Dynamics 365 data and the Dynamics 365 service-specific terms apply.

### When will my data be removed after I opt out of data sharing in Exchange?

If you're part of a security group that has been opted out by your administrator, the system can take up to 24 hours to remove data from all apps. It can take up to 30 days to remove backed-up data from Microsoft 365 storage accounts.  

If you've [opted out on your own](who-knows-whom.md#turn-off-data-sharing-with-dynamics-365-applications), the data is removed immediately.  

### How can an administrator opt out users?

The following administrators can opt out users at different levels:

- **Microsoft 365 Global administrator** can opt out users of a Microsoft 365 security group. For example, opt out groups such as C-suite, M&A, finance, and so on. More information: [Provide consent to collect data from Microsoft 365](provide-consent-office365.md)

- **Dynamics 365 administrator** can enable who knows whom for specific security roles to avoid opting in all Dynamics 365 users automatically. When you enable it for a specific role, the Exchange data is collected only from users who are part of the security role. More information: [Enable relationship intelligence](enable-ri.md)
