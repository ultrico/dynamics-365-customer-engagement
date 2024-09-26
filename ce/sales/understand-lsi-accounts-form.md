---
title: "Understand the LinkedIn Sales Insights tab in account forms (Dynamics 365 Sales) | MicrosoftDocs"
description: "Understand the LinkedIn Sales Insights tab in account forms in Dynamics 365 Sales."
ms.date: 10/25/2021
ms.topic: article
author: udaykirang
ms.author: udag
ms.reviewer: udag
ms.custom: 
  - dyn365-sales
---
# Understand the LinkedIn Sales Insights tab 

The **LinkedIn Sales Insights** tab in **Account** records provides information about the company and personas that are defined for the company within LinkedIn Sales Insights.

## License and role requirements
| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium or Dynamics 365 Sales Enterprise  <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | Any primary sales role, such as salesperson or sales manager<br>  More information: [Primary sales roles](security-roles-for-sales.md#primary-sales-roles)|



## LinkedIn Sales Insights entities

When the solution is installed, two new entities are created in Dynamics 365 Sales:

- LinkedIn Sales Insights Company Profile (one company profile record related to each account)
  > [!div class="mx-imgBorder"]
  > ![LinkedIn Sales Insights tab in an account form.](media/lsi-tab-account-only.png "LinkedIn Sales Insights tab in an account form")

- LinkedIn Sales Insights Personas (three persona records related to each account)
  > [!div class="mx-imgBorder"]
  > ![LinkedIn Sales Insights tab persona records.](media/lsi-tab-account-personas-records.png "LinkedIn Sales Insights tab persona records")

When CRM sync for LinkedIn Sales Insights is enabled, LinkedIn Sales Insights for Dynamics 365 brings data from all accounts that are matched in LinkedIn Sales Insights into account records in Dynamics 365. While configuring the data pipeline from LinkedIn, customers have the option to automatically update the data every 24 hours.

| Entities | Parameter information |
|----------|-----------------------|
| Company Profile |•  LinkedIn ID<br>•  Company Page URL<br>•  Company Name<br>•  Industry<br>•  Global Employee Count<br>•  Global Employee Growth (%)<br>•  Headquarters City<br>•  Headquarters State<br>•  Headquarters Country<br>•  Company Website URL<br>•  Last Update |
| Personas |•  Name<br>•  Employee Count<br>•  Employee Growth |

## Related information

[Install or delete the LinkedIn Sales Insights solution](install-lsi-solution.md)     
[LinkedIn Sales Insights for Dynamics 365 Sales - Installation Guide](https://www.linkedin.com/help/sales-navigator/answer/a419445)
