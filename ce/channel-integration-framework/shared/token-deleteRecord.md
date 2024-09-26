## Syntax

`Microsoft.CIFramework.deleteRecord(entityLogicalName, id).then(successCallback, errorCallback);`

## Parameters

| Name | Type  | Required  | Description |
| ---- | ----  | --------  | ----------- |
| entityLogicalName | String | Yes | The entity logical name of the record you want to delete. For example: "account".|
 | id   | String | Yes | GUID of the entity record you want to delete.| 
| successCallback | Function | No |  A function to call when a record is deleted. |
| errorCallback | Function  | No  | A function to call when the operation fails. |
||||

## Return Value

On success, returns a promise containing a string with the attributes and their values.

## Examples

This sample code deletes an existing contact record with record ID = a8a19cdd-88df-e311-b8e5-6c3be5a8b200

```JavaScript
// delete contact record  with the id=b44d31ac-5fd1-e811-8158-000d3af97055d
var id = "b44d31ac-5fd1-e811-8158-000d3af97055";
var entityLogicalName = "contact";
Microsoft.CIFramework.deleteRecord(entityLogicalName, id).then(
    function success(result) {
      res=JSON.parse(result);
      console.log("Contact deleted with ID: " + res.contactid);
      // the record is deleted
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```
