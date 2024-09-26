## Syntax

`Microsoft.CIFramework.renderSearchPage(entityLogicalName, searchString).then(successCallback, errorCallback);`

## Parameters

<table style="width:100%">
<tr>
<th>Name</th>
<th>Type</th>
<th>Required</th>
<th>Description</th>
</tr>
<tr>
<td>entityLogicalName</td>
<td>String</td>
<td>Yes</td>
<td>The entity logical name of the record you want to be queried. For example: &quot;account&quot;.</td>
</tr>
<tr>
<td>searchString</td>
<td>String</td>
<td>Yes</td>
<td>String to search among the attributes of the entity records.</td>
</tr>
<tr>
<td>successCallback</td>
<td>Function</td>
<td>No</td>
<td><p>A function to call when some records are retrieved.</p>
</td>
</tr>
<tr>
<td>errorCallback</td>
<td>Function</td>
<td>No</td>
<td>A function to call when the operation fails.</td>
</tr>
</table>

## Return value

<!--Editor note: "On success, returns a promise ..." What returns the promise? Need a noun.-->


On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.

## Example

The following example shows how to query for the term "Contoso" among the records of an Account entity.

```JavaScript
var entityname = "account"
var searchterm = "Contoso"

Microsoft.CIFramework.renderSearchPage(entityname, searchterm).then(
      function (success) {
        console.log(success);
    },
    function (error) {
        console.log(error);
    }
  );
```