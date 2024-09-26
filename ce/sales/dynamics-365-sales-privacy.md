---
title: Dynamics 365 Sales and privacy laws and regulations
description: To comply with privacy laws and regulations, we’ve made it possible to update read-only records through an export and import, and through SDKs.
ms.date: 07/06/2022
ms.topic: article
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
---
# Dynamics 365 Sales and privacy laws and regulations 

[!INCLUDE [gdpr-intro](~/../shared-content/shared/privacy-includes/gdpr-intro.md)]
 
To help comply with privacy laws and regulations, we've made it possible to edit read-only records in [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)].

The following table shows the states in which the [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] records become read-only. 

|  Entity  |  State  |
|  ------  |  -----  |
|  Quote   | Active/Closed |
|  Order   | Fulfilled/Canceled/Submitted/Invoiced |
|  Invoice | Paid/Canceled/Closed | 

A system administrator can export read-only quote, order, and invoice records, update them, and import the updated records back to [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)].  

It's also possible to update the read-only records programmatically with the SDK for Dynamics 365 Sales.

## Update read-only records through export or import

> [!IMPORTANT]
> Only an administrator or an impersonating user with administrative privileges can perform this action. Other users will get the following error message if they try to import records:
```Business Process Error: Cannot perform the action because the record is read only```

[!INCLUDE [gdpr-dsr-export-note](~/../shared-content/shared/privacy-includes/gdpr-dsr-export-note.md)]

1. In your sales app, go to the list of records. For example, go to **Sales** > **Quotes**.

2. Open the view that shows all the records regardless of their state. For example, open the **All Quotes** view.

3. Select the records that you want to export, and on the command bar, select **Export to Excel** > **Static Worksheet**. More information: [Export data to Excel](/powerapps/user/export-data-excel)

4. In the file that you exported, make the necessary changes.

5. To import the updated records back into [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)], in your sales app, in the list of records, select **Import Data**. More information: [Import data into Dynamics 365 Sales](import-data.md)


## Important points

- As a system administrator, you can edit any read-only field but changes won't reflect for the locked fields. 

- Non-admin users can't edit an active quote. However, an admin user can edit and save an active quote, although it's read-only for non-admin users.

- If configured, Plugins, Business processes and workflows run on fields getting updated or becoming editable. 

- If there is Dynamics 365 Sales integration with any third-party system, there's a chance that the privacy-related changes are overwritten if the correct sequence of updates isn't followed. It's the responsibility of the system administrator of Dynamics 365 Sales to follow the correct order.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
