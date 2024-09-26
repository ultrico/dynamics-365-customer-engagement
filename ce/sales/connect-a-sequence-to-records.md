---
title: Connect a sequence to records
description: Connect a sequence to a record based on the entity that the sequence is created in the sales accelerator in Dynamics 365 Sales.
ms.date: 09/17/2024
ms.topic: article
author: udaykirang
ms.author: udag
ms.reviewer: udag
---
# Connect a sequence to records 

After you create and activate a sequence for the selling process, you connect the sequence to records depending on the entity that you've created the sequence for. When a sequence is connected to an entity, the activities defined in the sequence will be shown in order on the record's **Summary** under **Up next** in **My work**.   

Also, you can connect multiple sequences to a record. More information: [Connect multiple sequences to record](#connect-multiple-sequences-to-record)

## License and role requirements
| Requirement type | You must have |
|-----------------------|---------|
| **License** | Dynamics 365 Sales Enterprise, Dynamics 365 Sales Premium, or [Microsoft Relationship Sales](https://dynamics.microsoft.com/en-in/sales/relationship-sales/) <br>More information: [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/sales/pricing/) |
| **Security roles** | System Administrator, Sequence Manager, or Salesperson <br>  More information: [Predefined security roles for Sales](security-roles-for-sales.md)|

## Connect multiple sequences to record

To improve the customer engagement and collaboration when multiple team members work on a record, you can connect multiple sequences to that record. This helps in closing deals faster, and bringing better business results.  
As a sales manager or seller, you can connect multiple sequences to a record manually. Select the **Connect sequence** option on the record page. In the **Connect *record* to sequence** dialog box, connect the required sequences. For connecting multiple sequences, verify that the record owner or the sequence owner has the [necessary permissions](create-manage-sequences.md#permission-requirements-to-manage-sequences).  
More information: [Through the record type grid view](#through-the-record-type-grid-view). 

>[!NOTE]
>When a segment is connected to the same sequence more than once for the same record and assigned to the same seller, the Up next widget displays duplicate activities.  

## Ways to connect sequence to records

You can connect a sequence to records in the following ways:  

- [Through a sequence](#ContactThroughASequence)
- [Through the record type grid view](#ContactThroughGridView)
- [Through a record](#ContactThroughARecord)
- [Through Power Automate](#through-power-automate)

<a name='ContactThroughASequence'></a>
## Through a sequence   

>[!NOTE]
>In this procedure, we're considering a sequence that was created based on **Lead** as an example. For sequences that are based on **Opportunity**, the procedure is similar.

1. Sign in to your sales app.   
2. Go to **Change area** in the lower-left corner of the page, and select **Sales Insights settings**.   
3. Under **Sales accelerator**, select **Sequences**.   
4. On the **Sequences** page, select and open the sequence that is active state.<br>or<br>Hover over the sequence, and then select **More options** > **View sequence**.    
    The sequence opens.    
    >[!NOTE]
    >You can assign records only to sequences that are in an **Active** state.
  
5. Select the **Connected *record*** tab. In this example, we're selecting a sequence with record type lead.     
    You can see the list of records that are connected to the sequence. If no records are connected, an empty section is displayed.   

    > [!div class="mx-imgBorder"]
    > ![Connected leads tab of a sequence](media/sequence-connected-sequence-tab.png "Connected leads tab of a sequence") 

7.	In the **Connected leads** section, select **+ Connect leads**.     
    The list that appears shows available lead records that aren't connected to any sequence.

    > [!div class="mx-imgBorder"]
    > ![List of available lead records](media/sequence-list-of-available-leads.png "List of available lead records") 

    > [!NOTE]
    > On the record selection page, you can do the following tasks on the grid:
    > - Sort and filter the records based on the column options. Select the down arrow icon corresponding to column header, and then select the sort and filter options that are available.
    > - Reorder the columns by dragging-and-dropping at the location you want in the grid.
    > - Search is available only on the name and description of the sequence.

8.	Choose the records that you want to connect to the sequence, and then select **Connect**.     
    Verify that the **Open leads without sequences** view is selected. Selecting this view helps to list only the records that aren't associated with other sequences. You can select other views to choose records to connect, but the records in that view must not be associated with other sequences.     
    > [!div class="mx-imgBorder"]
    > ![Select lead records to connect](media/sequence-select-leads-to-connect.png "Select lead records to connect")   

    The lead records are connected to the sequence and are added to the list of connected records.   
    > [!div class="mx-imgBorder"]
    > ![Lead records connected to sequence](media/sequence-leads-connected.png "Lead records connected to sequence")       
    
<a name='ContactThroughGridView'></a>
## Through the record type grid view   

1. Sign in to your sales app.   
2. Go to **Change area** in the lower-left corner of the page, and select **Sales**.   
3. Under **Sales**, select the record type such as, **Leads** or **Opportunities**, depending on the records you want to connect.   
    In this example, we select **Leads**.   
    > [!div class="mx-imgBorder"]
    > ![Lead view](media/sequence-connect-lead-view.png "Lead view")        
4. Select the records to which you want to connect the sequence. In this example, we select **Sharon Thonpson** and **Christopher Anderson**.   
    > [!div class="mx-imgBorder"]
    > ![Select leads to connect the sequence to](media/sequence-select-leads-connect-sequence.png "Select leads to connect the sequence to")   

    > [!NOTE]
    >- You can't connect a sequence to a record that has already been connected with a different sequence. When you select a record that was already connected, the **Disconnect sequence** option appears on the toolbar. To connect to a different sequence, select **Disconnect sequence**. The record will be available to connect to the sequence you want.      
    >- When you choose multiple sequences to connect, and the chosen list contains both connected and disconnected records, no option to connect or disconnect will be displayed on the toolbar.    
5. Select **Connect sequence**. The list of available sequences that appears includes sequences created by you and other sales managers.   
    In this example, a list of sequences that are configured for the **Lead** entity is displayed.    
    > [!div class="mx-imgBorder"]
    > ![List of sequences for leads](media/sequence-lead-list-sequence.png "List of sequences for leads")   
6. Select a sequence, and then select **Connect**.

A confirmation message appears at the bottom of the page, and the sequence is connected to the selected lead records. Now, sellers who have access to the lead record can see the activities connected with it.   

<a name='ContactThroughARecord'></a>
## Through a record   

1. Sign in to your sales app.   
2. Go to **Change area** in the lower-left corner of the page, and select **Sales**.   
3. Under **Sales**, select **Leads** or **Opportunities**, depending on the records you want to connect.   
    In this example, we select **Leads**.   
    > [!div class="mx-imgBorder"]
    > ![Lead view](media/sequence-connect-lead-view.png "Lead view")       
4. Open the record to which you want to connect the sequence. In this example, we opened the lead **Sharon Thonpson**.   
    > [!div class="mx-imgBorder"]
    > ![Open a lead to connect the sequence to](media/sequence-open-lead-connect-sequence.png "Open a lead to connect the sequence to")   
    > [!NOTE]
    >  When you select a record that was already connected, the **Disconnect sequence** option appears on the toolbar. Disconnect the record from the sequence it's currently connected with, and then connect it to the sequence you want. More information: [View details of a sequence and its connected records](view-sequence-details-connected-records.md)       
5. Select **Connect sequence**. The list of available sequences that appears includes sequences created by you and other sales managers.   
    In this example, a list of sequences that are configured for the **Lead** entity is displayed.    
    > [!div class="mx-imgBorder"]
    > ![List of sequences for leads](media/sequence-lead-list-sequence.png "List of sequences for leads")    
6. Select a sequence, and then select **Connect**.

A confirmation message appears at the bottom of the page, and the sequence is connected to the selected lead records. Now, sellers who have access to the lead record can see the activities connected with it.

## Through Power Automate

You can create a flow based on a sequence. The flow connects the records automatically to the sequence when the trigger satisfies the flow condition.

1.	Go to [Microsoft Power Automate](https://flow.microsoft.com), and sign in with your Dynamics 365 credentials.    
    >[!NOTE]
    >By default, your organization is selected based on your latest association. If you have multiple organizations associated with you, select the proper organization from your profile settings.    
2.	Select **Solutions**, and then select **Default Solution**.    
    > [!div class="mx-imgBorder"]
    > ![Select the default solution in Power Automate](media/sequence-power-automate-select-solution.png "Select the default solution in Power Automate")    
    All default solutions are listed.
3.	In the search box on the toolbar, search for the flow that you want update or view.     
    > [!div class="mx-imgBorder"]
    > ![Search for your solution](media/si-admin-view-flows-search-solution.png "Search for your solution")
4. Configure a trigger to the flow.    
5. Select **New step**.   
6. In the **Search connectors and actions** box, select **Microsoft Dataverse**, and then search for and add the action **Perform an unbound action**.     
    > [!div class="mx-imgBorder"]
    > ![Search and add Perform an unbound action](media/sequence-add-an-unbound-action.png "Search and add Perform an unbound action")     
7.	In the **Perform an unbound action** step, select the **Action Name** as **msdyn_ConnectSequence**.     
    > [!div class="mx-imgBorder"]
    > ![Select the action name](media/sequence-select-action-name.png "Select the action name")       
    Enter the following additional information:     
    -	**RegardingEntityId**: The unique identifier of the entity record that is to be connected to the sequence.    
    -	**RegardingEntityName**: The logical name of the entity.    
    -	**SequenceId**: The unique identifier of the sequence.       
    - **SegmentId**: (Optional) The unique identifier of the segment.
    - **Source**: (Optional) The source of the record.
    -  **WaitTime**: (Optional) The time to wait before connecting the record to the sequence.
    - **AdvancedToOtherSequenceTargetStepld**: (Optional) The unique identifier of the sequence step to which the record is to be advanced to another sequence.

    >[!NOTE]
    >To get the unique identifier of the sequence, query OData for the sequence entity (msdyn_sequence). More information: [Querying or browsing an OData endpoint](/dynamics365/fin-ops-core/dev-itpro/data-entities/odata#querying-or-browsing-an-odata-endpoint)
    
8. Use **Flow Checker** to verify errors and warnings in the flow.   
    Errors and warnings in the flow cause performance or reliability issues. Ensure that the flow is free from errors and warnings. The checker is always active, appearing in the command bar in the designer. The checker shows a red dot when it finds one or more errors in your flow.   
    For example, while creating a **For due date coming up** card, you haven't entered **Card Name**. The flow checker identifies the error and displays a red dot.     
    > [!NOTE]
    > You must resolve all errors and warnings to save the flow.     
9. (Optional) Select **Test** to test your flow.     
    Ensure that all the configured steps are working as required. The test feature runs and validates each step in the flow, and highlights any step that contains an error. You must resolve the error to proceed.    
    Select an option to test the flow by triggering actions or by using the data from previous test runs, and then select **Save & Test**.     
    > [!div class="mx-imgBorder"]   
    > ![Select Test flow type](media/si-admin-create-flow-select-test-flow.png "Select Test flow type")           
10. Save and publish the flow.

[!INCLUDE[cant-find-option](../includes/cant-find-option.md)]

## Related information

[Sequences](create-manage-sequences.md)  
[Create and activate a sequence](create-and-activate-a-sequence.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
