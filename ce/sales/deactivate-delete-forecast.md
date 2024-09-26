---
title: "Deactivate and delete a forecast in Dynamics 365 Sales"
description: "Deactivate and delete a forecast in Dynamics 365 Sales."
ms.date: 10/26/2021
ms.topic: article
author: lavanyakr01
ms.author: lavanyakr
ms.reviewer: lavanyakr
---
# Deactivate and delete forecasts 

You can deactivate or delete forecasts that are no longer required in your organization.  

## License and role requirements
| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium or Dynamics 365 Sales Enterprise  <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | System Administrator or Forecast Manager <br> More information: [Predefined security roles for Sales](security-roles-for-sales.md)|


## Deactivate a forecast 

You can deactivate forecasts that are that are no longer required in your organization. You can view the list of deactivated forecasts under the **Inactive** tab.

> [!IMPORTANT]
> - You can't activate a forecast after you deactivate it.
> - Don’t deactivate a forecast through any other options such as **Advanced find**. Use only forecast configuration page to deactivate forecasts. 
 
1.	Open the **Forecast configuration** page.

    The forecast configuration page opens.

    > [!div class="mx-imgBorder"]
    > ![Forecast home page.](media/forecast-deactivate-home-page.png "Forecast home page")
 
2.	Select the **More options** icon corresponding to the forecast that you want to deactivate, and then select **Deactivate**.
 
    > [!div class="mx-imgBorder"]
    > ![Select deactivate for a forecast.](media/forecast-deactivate-select-deactivate.png "Select deactivate for a forecast")

    A confirmation message is displayed.

    > [!div class="mx-imgBorder"]
    > ![Select deactivate on confirmation message.](media/forecast-deactivate-confirm-deactivate.png "Select deactivate on confirmation message")

3.	Select **Deactivate**.

    The forecast is deactivated and listed under the **Inactive** tab.

    > [!div class="mx-imgBorder"]
    > ![View deactivated forecasts under inactive tab.](media/forecast-deactivate-inactive-tab.png "View deactivated forecasts under inactive tab") 

## Delete a forecast

You can permanently delete a forecast that is in the active, inactive, or draft state.

1.	Open the **Forecast configuration** page.

    The forecast configuration page opens.

    > [!div class="mx-imgBorder"]
    > ![Forecast home page.](media/forecast-deactivate-home-page.png "Forecast home page")
 
2.	Select the **More options** icon corresponding to the forecast that you want to deactivate, and then select **Delete**.

    > [!div class="mx-imgBorder"]
    > ![Select delete for a forecast.](media/forecast-delete-select-delete.png "Select delete for a forecast")

    A confirmation message is displayed.

    > [!div class="mx-imgBorder"]
    > ![Select delete on confirmation message.](media/forecast-delete-confirm-delete.png "Select delete on confirmation message")

3.	Select **Delete**.

    The forecast is deleted permanently from your organization.

[!INCLUDE[cant-find-option](../includes/cant-find-option.md)] 

## Related information

[Activate and upload simple columns data](activate-upload-simple-columns-data-forecast.md)   
[Configure forecasts in your organization](configure-forecast.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
