Using the Dynamics 365 Channel Integration Framework solution, you can configure channel providers.
To configure channel providers:

1. Sign in to Dynamics 365.

2. Select the dropdown button on the Dynamics 365 and select **Channel Integration Framework**.

  ![Dynamics 365 dropdown button to find Channel Integration Framework.](../media/cif-app-navigation.png "Dynamics 365 drop-down button to find Channel Integration Framework")

3.	Select **+ New** to add a new provider.

4.	In the **New Channel** page, specify the following:

  | Field | Description |
  |-------|-------|
  |Name|Name of the channel provider.|
  |Label|The label is displayed as the title on the widget.|
  |Channel URL|The URL of the provider to host in the widget. See the JavaScript APIs on how to develop communication widget with Dynamics 365 Channel Integration Framework.|
  |Enable Outbound Communication|When a phone number is selected on the Dynamics 365 Unified Interface page, the widget initiates the call or outbound communication.|
  |Channel Order|The order of precedence of the channel providers.|
  |API Version|The version of the Channel Integration Framework APIs.|
  |Trusted Domain| An additional domain if the initial landing URL and the final domain from which the communication widget is hosted are different. Add the domain (URL) to access the Channel Integration Framework APIs. |
  |Select the Unified Interface Apps for the Channel| The list of Unified Interface apps where the channel is displayed for the agents. |
  |Select Roles for the Channel|The security roles that are present in Dynamics 365.<br>**Note:** If you do not assign any role, the channel provider is shown to all users assigned for the Dynamics 365 Unified Interface app.|
  |Custom Parameter|This takes a text blob as input and `Microsoft.CIFramework.getEnvironment` will return this as value of key `customParams`.|
  
  ![Channel provider configuration.](../media/channel-provider-configuration.PNG "Channel provider configuration")

  > [!Note]
  > The msdyn_ciprovider entity is accessible only for the administrator roles and hence the panel will not load for a non-administrator roles. To load the panel for the non-administrator roles, create a new role and provide read-access to the msdyn_ciprovider entity. Now, add the role to the users who will be accessing the Channel Integration Framework.

5. Launch the Unified Interface App to see the communication widget on the right side.<br><br>
