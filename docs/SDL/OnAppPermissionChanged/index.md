## OnAppPermissionChanged

Type
: Notification

Sender
: SDL

Purpose
: Inform HMI that permissions have changed for a specified application.

### Notification

#### Parameters

|Name|Type|Mandatory|Additional|
|:---|:---|:--------|:---------|
|appID|Integer|true||
|isAppPermissionsRevoked|Boolean|false||
|appRevokedPermissions|[Common.PermissionItem](../../common/structs/#permissionitem)|false|array: true<br>minsize: 1<br>maxsize: 100|
|appRevoked|Boolean|false||
|appPermissionsConsentNeeded|Boolean|false||
|appUnauthorized|Boolean|false||
|priority|[Common.AppPriority](../../common/enums/#apppriority)|false||
|requestType|[Common.RequestType](../../common/enums/#requesttype)|false|array: true<br>minsize: 0<br>maxsize: 100|  
|requestSubType|String|false|array: true<br> minsize: 0<br> maxsize: 100 <br> maxlength: 100|The list of SystemRequest's requestSubTypes allowed by policies for the named application.<br>If the app sends a requestSubType which is not specified in this list, then that request should be rejected.<br>An empty array signifies that any value of requestSubType is allowed for this app.<br> If this parameter is omitted, then a request with any value of requestSubType is now allowed for this app|


### Sequence Diagrams
|||
OnAppPermissionChanged with consent required
![OnAppPermissionChanged](./assets/OnAppPermissionChanged.png)
|||

#### JSON Example Notification
```json
{
  "jsonrpc" : "2.0",
  "method" : "SDL.OnAppPermissionChanged",
  "params" :  
  {
    "appID" : 65674,

  }
}
```
