---
title: Create custom push notifications for the Dynamics 365 Sales mobile app
description: Learn to create custom push notifications for the Dynamics 365 Sales mobile app.
ms.date: 08/29/2024
ms.topic: article
author: sbmjais
ms.author: shjais
ms.reviewer: shjais 
---

# Create custom push notifications 

Push notifications help to engage app users and help them prioritize key tasks. 

## License and role requirements

| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Premium, Dynamics 365 Sales Enterprise, Dynamics 365 Sales Professional, or Microsoft Relationship Sales <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | System administrator <br>  More information: [Predefined security roles for Sales](../security-roles-for-sales.md)|


## About push notifications

The Dynamics 365 Sales mobile app supports push notifications that can be created by using the **Send push notification V2** action with the following details:

- **Mobile app**: Select **Sales**.
- **Your app**: Select the app that you want to set up the notification for.
- **Recipients Item-1**: Enter the user's email or the user's Microsoft Entra ID object ID.
- **Message**: Enter the notification message.
- **Open app**: Select **Yes**.
- **Entity**:  Select which table the notification is for.
- **Record ID**: Enter the record ID. If you don't enter a record ID, the mobile app will open at the home screen when you tap the notification. If you enter the record ID, the mobile app will open the specified record when you tap the notification.

![Send push notification V2 action.](media/sm-push-notif.png "Send push notification V2 action")

For information about creating push notifications, go to [Create push notifications for Power Apps mobile](/powerapps/mobile/power-apps-mobile-notification).

## Validate your flow

1. Sign in to [Power Automate](https://flow.microsoft.com).

2. On the left pane, select **My flows**, and then select a flow.

    ![Select a flow.](media/select-flow.png "Select a flow")

3. From the run history, select an instance of the run.

    ![Run history of a flow.](media/flow-run-history.png "Run history of a flow")

4. Validate the inputs passed during the run.

    ![Validate the inputs of a flow.](media/flow-inputs.png "Validate the inputs of a flow")


## Related information

[Use the Dynamics 365 Sales mobile app](use-sales-mobile-app.md)    
[Learn the basics](learn-basics-mobile-app.md)

