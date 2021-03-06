# getVqdTemplate


## Description
Search video quality detection templates

## Request Method
GET

## Request Address
https://vqd.jdcloud-api.com/v1/vqdTemplates/{templateId}


## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**templateId**|String|True| |Template ID, path parameter|


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](getvqdtemplate#result)|Result of searching video quality detection template information|
|**requestId**|String|Request ID|

### <div id="result">Result</div>
|Name|Type|Description|
|---|---|---|
|**templateId**|String|Template ID|
|**templateName**|String|Template Name. Length cannot exceed 128 characters. UTF-8 code. <br>|
|**threshold**|Double|Defect determination temporal threshold|
|**detections**|String[]|List of Test Items|
|**createTime**|String|Creation Time|
|**updateTime**|String|Modification Time|

## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|

## Request Example
GET
```
https://vqd.jdcloud-api.com/v1/vqdTemplates/10000

```

## Return Example
```
{
    "requestId": "bgvmivir54gddpgi764se9f4kfr7ge41", 
    "result": {
        "createTime": "2019-04-16T15:51:32Z", 
        "detections": [
            "BlackScreen", 
            "ColorCast"
        ], 
        "templateId": "10000", 
        "templateName": "Template-10000", 
        "threshold": "3.000", 
        "updateTime": "2019-04-16T15:51:32Z"
    }
}
```
