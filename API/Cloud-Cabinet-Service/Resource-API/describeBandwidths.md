# describeBandwidths


## 描述
查询带宽（出口）列表

## 请求方式
GET

## 请求地址
https://jdccs.jdcloud-api.com/v1/idcs/{idc}/bandwidths

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**idc**|String|True| |IDC机房ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**pageNumber**|Integer|False|1|页码, 默认为1|
|**pageSize**|Integer|False|20|分页大小，默认为20|
|**filters**|[Filter[]](#filter)|False| |bandwidthId - 带宽实例IID，精确匹配，支持多个<br>|

### <div id="Filter">Filter</div>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|True| |过滤条件的名称|
|**operator**|String|False| |过滤条件的操作符，默认eq|
|**values**|String[]|True| |过滤条件的值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|[Result](#result)| |
|**requestId**|String|请求ID|

### <div id="Result">Result</div>
|名称|类型|描述|
|---|---|---|
|**bandwidths**|[DescribeBandwidth[]](#describebandwidth)|带宽（出口）列表|
|**pageNumber**|Integer|页码|
|**pageSize**|Integer|分页大小|
|**totalCount**|Integer|总数量|
### <div id="DescribeBandwidth">DescribeBandwidth</div>
|名称|类型|描述|
|---|---|---|
|**idc**|String|机房英文标识|
|**idcName**|String|机房名称|
|**bandwidthId**|String|带宽实例ID|
|**bandwidthName**|String|带宽名称|
|**status**|String|状态 normal:正常 abnormal:异常|
|**lineType**|String|线路类型 dynamicBGP:动态BGP thirdLineBGP:三线BGP telecom:电信单线 unicom:联通单线 mobile:移动单线|
|**chargeType**|String|计费方式 fixedBandwidth:固定带宽 95thPercentile:95峰值 merge95thPercentile:合并95峰值|
|**bandwidth**|Integer|合同带宽（Mbps）|
|**relatedIp**|[RelatedIp[]](#relatedip)|关联的公网IP|
### <div id="RelatedIp">RelatedIp</div>
|名称|类型|描述|
|---|---|---|
|**cidrAddr**|String|IP地址段|
|**lineType**|String|线路类型 dynamicBGP:动态BGP thirdLineBGP:三线BGP telecom:电信单线 unicom:联通单线 mobile:移动单线|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
