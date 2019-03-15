# describeLiveTimeshiftConfigs


## 描述
查询时移配置

## 请求方式
GET

## 请求地址
https://live.jdcloud-api.com/v1/liveTimeshift:configs


## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**pageNum**|Integer|False|1|页码；默认为1；取值范围[1, 100000]|
|**pageSize**|Integer|False|10|分页大小；默认为10；取值范围[10, 100]|
|**playDomain**|String|True| |直播的推流域名|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result| |
|**requestId**|String|ruquestId|

### Result
|名称|类型|描述|
|---|---|---|
|**pageNumber**|Integer|当前页码|
|**pageSize**|Integer|每页数量|
|**totalCount**|Integer|查询总数|
|**timeshiftConfigs**|TimeshiftConfig[]|直播时移集合|
### TimeshiftConfig
|名称|类型|描述|
|---|---|---|
|**publishDomains**|ShiftPublishDomain[]|推流域名集合|
|**playDomains**|ShiftPlayDomain[]|直播域名集合|
### ShiftPlayDomain
|名称|类型|描述|
|---|---|---|
|**playDomain**|String|直播播放域名|
|**timeshiftStatus**|String|直播时移状态:<br>  - on表示开启<br>  - off表示关闭<br>|
|**playType**|String|播放域名类型:<br>  - normal  一般的播放域名<br>  - restart 回看播放域名<br>|
### ShiftPublishDomain
|名称|类型|描述|
|---|---|---|
|**publishDomain**|String|直播推流域名|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|
