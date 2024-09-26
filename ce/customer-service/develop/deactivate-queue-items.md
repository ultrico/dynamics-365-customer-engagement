---
title: Close live work items or deactivate queue items
description: Sample code to close live work items or deactivate queue items.
ms.date: 07/31/2024
ms.topic: reference
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.custom: 
  - dyn365-customerservice
search.audienceType: 
  - developer
  - customizer
---

# How to close live work items or deactivate queue items

You can use the following sample code in your Console App (.NET framework) of Visual Studio to trigger the closure of live work items by deactivating the associated queue item.

For information about how you can modify the sample code to suit your environment, go to [Quickstart: Organization service sample (C#)](/powerapps/developer/data-platform/org-service/quick-start-org-service-console-app).

   ```csharp
    static void Main(string[] args)
    {
        // e.g. https://yourorg.crm.dynamics.com
        string url = "<your environment url>";
        // e.g. you@yourorg.onmicrosoft.com
        string userName = "<your user name>";
        // e.g. y0urp455w0rd 
        string password = "<your password>";
    
        string conn = $@"
        Url = {url};
        AuthType = OAuth;
        UserName = {userName};
        Password = {password};
        AppId = 51f81489-12ee-4a9e-aaae-a2591f45987d;
        RedirectUri = app://58145B91-0C36-4500-8554-080854F2AC97;
        LoginPrompt=Auto;
        RequireNewInstance = True";

        using (var svc = new CrmServiceClient(conn))
        {

            WhoAmIRequest request = new WhoAmIRequest();
    
            WhoAmIResponse response = (WhoAmIResponse)svc.Execute(request);
    
            Console.WriteLine("Your UserId is {0}", response.UserId);
    
            try
            {
                //Provide queueitem id as the second parameter which has to be deactivated.
                svc.UpdateStateAndStatusForEntity("queueitem", new Guid("6f15a7f0-8788-eb11-a812-000d3a593524"), 1, 2);
            }
            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
            }

            Console.WriteLine("Press any key to exit.");
            Console.ReadLine();
        }
    }
   ```



### Related information

[Overview of unified routing](../administer/overview-unified-routing.md)  
[Set up unified routing](../administer/set-up-routing-process.md)  
[How unified routing affects queue items and the corresponding APIs](unified-routing-impact-on-APIs.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
