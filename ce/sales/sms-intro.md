---
title: Engage with customers through text messages
description: Enable your sellers to send text messages (SMS) to customers and refer previous communications in context without leaving the application or losing view of customers' details.
ms.date: 02/16/2024
ms.topic: overview
author: udaykirang
ms.author: udag
ms.reviewer: udag
ms.custom: 
  - bap-template
  - references_regions
---

# Engage with customers through text messages

Sending and receiving text messages through SMS is an effective way for sellers to reach out to potential customers. It's fast, convenient, and allows for quick responses. Sellers use SMS to stay in touch with their customers, by responding to questions or concerns, and providing updates and information on products and services.  

Dynamics 365 Sales enables your sellers to send and receive SMS from customers through the text message feature. Also, sellers can refer to their past communication in context without leaving the application or losing their view of their customers' details. To ensure professional and secure communication, the application always prioritizes business phone numbers over personal ones when sending automated SMS.  

In the sequences, SMS can be included as a step to send reminders or updates about key events. 

>[!NOTE]
>The text message feature is only supported in web browsers.

## How can I use the text message feature?

Depending on your role, you can use the text message feature as described in the list:

-	System administrator or similar role:
    -	Configure the SMS provider in your organization for sellers to use. More information: [Configure SMS provider](configure-sms-provider.md)
    -	Assign or remove phone numbers of users. More information: [Edit phone numbers](edit-phone-numbers.md)
    -   Add the text message option to custom forms. More information: [Add text message option to custom forms](add-sms-option-custom-forms.md)   
          
- 	Sales manager, seller, or any other similar role: 
    -	Choose a service provider to send and receive SMS. More information: [Understand the conversation pane](manage-text-message-communications.md#understand-the-conversation-pane)
    -	Add text message and automated text message as steps in a sequence. More information: [Send a text message](steps-sequence.md#send-a-text-message) and [Send an automated text message](steps-sequence.md#send-an-automated-text-message)
    -	Create and add SMS templates. More information: [Personalize text messages through templates](create-text-message-templates.md)
    -	Send SMS from the Sales accelerator workspace or the Up next widget. More information: [Send a text message to customers](connect-with-customers.md#send-a-text-message-to-customers)
    -	Access past SMS interactions in context with relevant sales records such as lead and opportunity. More information: [Manage text message conversations](manage-text-message-communications.md)

## In which regions is the text message feature available?

The text message feature is available in the following regions:

- Asia Pacific (APAC)
- Canada (CAN)
- Europe (EUR)
- France (FRA)
- Great Britain (GBR)
- India (IND)
- Japan (JPN)
- North America (NAM)
- Oceania (OCE)
- South America (SAM)
- Switzerland (CHE)
- United Arab Emirates (UAE)

>[!NOTE]
>Currently, the text message feature is not available in the following datacenters&mdash; Germany, China, South Africa, Korea, Norway, and Government Community Cloud (GCC), including USG, Department of Defense (DoD).

## Permissions required 

Verify that the users who need to use the text message feature have the following permissions.

>[!NOTE]
>If you’ve already enabled Sales accelerator and provided access to the required security roles, no additional permissions are required for the SMS feature. To provide permissions in Sales accelerator, see [Sales accelerator first-run setup](enable-configure-sales-accelerator.md#first-run-setup). 

**For salesperson or similar role**:<a name="salesperson-roles-sms-feature"></a>

| Tab name | Entity name | Access level | Privileges required |
|----------|-------------|--------------|---------------------|  
| Core Records | - Activity<br>- Note | User | - Create<br>- Write<br>- Delete<br>- Append |
| Core Records | - Activity<br>- Note | Business Unit | Read | 
| Core Records | Lead | Business Unit | - Create<br>- Read | 
| Custom Entities | Channel Instance | User | Append To |
| Custom Entities | - Channel Instance<br>- Channel Instance Account<br>- Channel Definition<br>- SalesOmnichannel Message<br>- Transcript | Business Unit | Read |
| Custom Entities | - Environment variable definition<br>- Consuming Application | Organization | Read |
| Custom Entities | Model-driven App User Setting | Organization | - Create<br>- Read<br>- Write<br>- Append |
| Custom Entities | Notification | User | Read |
| Custom Entities | SalesOmnichannel Message | User | - Create<br>- Write<br>- Delete<br>- Append<br>- Assign |
| Custom Entities | Setting definition | Organization | - Read<br>- Append |
| Custom Entities | Text message template | Business Unit | - Create<br>- Write<br>- Read<br>- Delete |
| Custom Entities | Transcript | User | - Create<br>- Write<br>- Delete<br>- Append<br>- Append To |

**For sales manager, sequence manager, or similar role**:

The following roles are required along with the roles defined in the [salesperson section](#salesperson-roles-sms-feature):

| Tab name | Entity name | Access level | Privileges required |
|----------|-------------|--------------|---------------------|  
| Custom Entities | Channel Instance | Business Unit | - Assign<br>- Write |
| Custom Entities | - Channel Definition locale<br>- Telesign channel instance account<br>- Twilio channel instance account | Business Unit | Read |
| Custom Entities | - Telesign channel instance<br>- Twilio channel instance | Business Unit | - Read<br>- Write<br>- Assign |

## Related information

[Configure SMS provider](configure-sms-provider.md)    
[Edit phone numbers](edit-phone-numbers.md)  
