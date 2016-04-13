## Alert

### Request
#### Parameters
|Name|Type|Mandatory|Additional|Description|
|:---|:---|:--------|:---------|:----------|
|alertStrings|Common.TextFieldStruct|true|array: true<br>minsize: 0<br>maxsize: 3||
|duration|Integer|true|minvalue: 3000<br>maxvalue: 10000||
|softButtons|Common.SoftButton|false|array: true<br>minsize: 0<br>maxsize: 4||
|progressIndicator|Boolean|false|||
|alertType|Common.AlertType|true|||
|appID|Integer|true|||
#### TextFieldStruct
|Name|Type|Mandatory|Additional|Description|
|:---|:---|:--------|:---------|:----------|
|fieldName|Common.TextFieldName|true|||
|fieldText|String|true|maxlength: 500||
#### SoftButton
|Name|Type|Mandatory|Additional|Description|
|:---|:---|:--------|:---------|:----------|
|type|Common.SoftButtonType|true|||
|text|String|false|maxlength: 500||
|image|Common.Image|false|||
|isHighlighted|Boolean|false|||
|softButtonID|Integer|true|minvalue: 0<br>maxvalue: 65535||
|systemAction|Common.SystemAction|true|||
#### AlertType
|Name|Value|
|:---|:----|
|UI|0|
|BOTH|1|
### Response
#### Parameters
|Name|Type|Mandatory|Additional|Description|
|:---|:---|:--------|:---------|:----------|
|tryAgainTime|Integer|false|minvalue: 0<br>maxvalue: 2000000000||