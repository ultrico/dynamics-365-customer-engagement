---
title: "Associate templates with scenarios  | MicrosoftDocs"
description: "Learn how to associate templates with scenarios in Dynamics 365 Channel Integration Framework 2.0."
author: gandhamm
ms.author: mgandham
ms.topic: article
ms.date: 03/12/2024
---

# Associate templates with scenarios

After creating the session, notification, and application tab templates, you must associate these with your scenarios so that the notification template is used for an incoming conversation. After an agent accepts the conversation, a session starts for which the session template is used. In the session, certain application tabs are required such as Knowledge article search and Case page. These application tabs are configured using the application tab templates and are associated with a session.

To associate the templates in your scenarios, you must use the `templateName` parameter in your code. For more information on notification, session, and application tab management APIs, see [JavaScript API Reference](../develop/reference/microsoft-ciframework-v2.md).


## See also

[Manage session templates](session-templates-cif.md)

[Manage application tab templates](application-tab-templates-cif.md)

[Manage notification templates](notification-templates-cif.md)

[Use automation dictionary to pass data parameter keys](automation-dictionary-keys-cif.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
