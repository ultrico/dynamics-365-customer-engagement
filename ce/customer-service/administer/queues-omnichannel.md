---
title: Create and manage queues for unified routing
description: Create and manage advanced queues, know how fallback and default queues work in unified routing in Customer Service.
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.topic: how-to
ms.date: 06/14/2024
ms.custom: bap-template
ms.collection:
searchScope:
- D365-App-customerservice
- D365-Entity-queueitem
- D365-UI-*
- Customer Engagement
- Dynamics 365
- Customer Service
---

# Create and manage queues for unified routing

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability-embedded-yes.md)]

Queues are used to collect and distribute workload among agents. Workload includes records such as cases, and conversations such as chat or SMS. Agents are added as members to the queues and the workload is distributed among the agents based on assignment methods.

## How work items are routed to queues

You can create separate queues for each line of business such as billing, investment, and products. When a customer query is raised for any of the areas, it's routed to the corresponding designated queue based on how you define route to queues in the classification. You can also set up a customer support availability matrix by using a combination of queues, operating hour schedules, and routing rules.

In an enterprise scenario, you can have various supervisors handling different issues, and therefore, different types of queues are required to handle the various scenarios. Accordingly, routing rules are set up based on the complexity of issues that need to be handled.

To simplify the routing experience for administrators and supervisors, queues are categorized based on the channel types as follows:

- **Messaging**: To route all messaging conversations pertaining to the live chat, SMS, and social channels.
- **Records**: To route work items pertaining to records, such as cases and emails.
- **Voice**: To route calls made to support phone numbers listed on the customer portal.

The queue types allow issues to be routed correctly and help avoid cross-queue assignments. When you configure workstreams and routing rule items, the queues that are available for selection are based on the channel type for the workstream. For example, for routing rules for a live chat workstream, only messaging type queues are shown for selection. Similarly, you can transfer a chat conversation only to a messaging queue, and a case only to a record queue.

Assign a group number that helps you organize your queues in the list view. The group number doesn't affect the priority of the queue or incoming conversations.

## Create a queue for unified routing

1. In the site map of Customer Service admin center, select **Queues** in **Customer support**.
    
1. On the **Queues** page, select **Manage** for **Advanced queues**.
    
1. On the **Queues** page, do the following steps:

    1. Select **New**.
    2. In the **Create a queue** dialog, enter the following details:
       - **Name**: A name for the queue.
       - **Type**: Select **Messaging**, **Record**, or **Voice**.
       - **Group number**: A number to organize the queue.
    3. Select **Create**. The queue that you created is displayed.

       > [!div class=mx-imgBorder]
       > ![Queue in admin center.](../media/queue-summary-ur.png "Queue in admin center")

1. Select **Add users**, and in the flyout menu, select the users who should be part of the queue, and then select **Add**. The users are added to the queue.

1. In **Assignment method**, select any of the following options:
   - **Highest capacity**: Assigns a work item to an agent with the highest available capacity. This agent has the skills that are identified during the classification stage and presence that matches one of the allowed presences in the workstream.
   - **Advanced round robin**: Assigns a work item to the agent who matches the criteria for skills, presence, and capacity. The initial order is based on when a user is added to the queue. Then, the order is updated based on assignments.
   - **Least active**: Assigns a work item to the agent who has been least active among all the agents who match skills, presence, and capacity.
   - **Create new**: Lets you create a custom assignment method. The custom assignment method lets you use your own rulesets and rules to configure priority, severity, and capacity for choosing the queues to which work items need to be routed by setting up the rulesets for prioritization and assignment. For more information about the custom assignment method, see [Create custom assignment method](assignment-methods.md).

1. To manage overflow of queues, in **Overflow management**, select **Set overflow conditions**, and perform the steps described in [Manage overflow of queues](manage-overflow.md).

1. To set the operating hours, in **Operation hours**, select **Set operation hours**. If you don't set operation hours, the queue is considered to be available round the clock. You must configure the operating hour record before you can set it for the queue. More information: [Configure operating hour record](create-operating-hours.md)

1. On the **Set operation hours** dialog that appears, select an operating hour record in the **Name** list.

1. Select **Save and close**. The operating hour record that you selected is configured for the queue.

### Manage queues for unified routing

You can manage queues on the **Queues** page, and perform operations such as search, edit, copy, and delete the queues.

- Select a queue to edit the users, assignment methods, or operating hour record.

- Select a queue on the **Queues** page, select **Copy** on the command menu, and then select **Copy** in the *<queue_name>* dialog. The queue is copied and inherits the settings of the queue you copied from, including its name, prefixed with **Copy of**.

> [!IMPORTANT]
> If unified routing is enabled, make sure that the **Queue** form, which is the default form, exists and hasn't been removed through customization. Otherwise, you aren't able to create a basic queue in Customer Service Hub.

### How fallback queues work

To efficiently manage the work items, you can configure a fallback queue per workstream that acts as a safety net. You can set an existing queue as the fallback queue or create a fallback queue with the required settings when you're creating a workstream.

For existing workstreams, you can configure the fallback queue on the workstream page. If you choose to create a queue, you need to add users. By default, the assignment method for the fallback queue is highest capacity.

If any overflow settings exist, they are overruled and work items are routed to the fallback queues in the following scenarios:

- Work item encounters an error during classification.
- Work item encounters an error when running a route-to-queue rule.
- Work item doesn't match any route-to-queue rules.

### How default queues work

Default queues are a finite set of system-defined queues that help you manage work items when other queues aren't available for routing them. All agents who have the Omnichannel agent role are a part of the default queues. Out of the box, the following default queues are available:

- **Default entity queue** for routing entity records.
- **Default messaging queue** for routing all messaging conversations pertaining to live chat, SMS, Microsoft Teams, and social channels.
- **Default voice queue** for routing all voice calls.

For a workstream, you can set any queue as a fallback queue, including a default queue but vice versa isn't possible. You can update the assignment method only for the default queues. However, we recommend that you always create advanced queues and define the assignment strategy instead of using the default queues. No other settings are available to edit.

### Related information

[Create and manage workstreams](create-workstreams.md)  
[Create and manage assignment methods](configure-assignment-rules.md#create-an-assignment-method-and-configure-rules)  
[Create and manage operating hours](create-operating-hours.md)  
[Configure the voice queues](../voice-channel-route-queues.md)  
[FAQ about time taken by configuration changes in unified routing](faqs.md#how-long-does-a-configuration-change-to-the-omnichannel-for-customer-service-and-unified-routing-settings-take-to-update)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
