## Syntax

`Microsoft.CIFramework.getClickToAct(value).then(successCallback, errorCallback);`

## Parameters

| Name            | Type     | Required | Description                                       |
|-----------------|----------|----------|---------------------------------------------------|
| successCallback | Function | No       | A function to call when the request is successful |
| errorCallback   | Function | No       | A function to call when the request fails         |

## Return value

**Type:** Boolean

**Description:** Returns Promise object with the value. True if **ClickToAct** is enabled; false otherwise.
