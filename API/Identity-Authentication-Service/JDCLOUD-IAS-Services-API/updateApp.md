# updateApp


## 描述
更新app

## 请求方式
PUT

## 请求地址
https://ias.jdcloud-api.com/v1/regions/{regionId}/app/{clientId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**clientId**|String|True| | |
|**regionId**|String|True| | |

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**accessTokenValiditySeconds**|Integer|False| |accessTokenValiditySeconds|
|**clientName**|String|False| |应用名|
|**clientUri**|String|False| |clientUri|
|**contacts**|String|False| |contacts|
|**extension**|String|False| |extension|
|**grantTypes**|String|False| |grantTypes|
|**jwks**|String|False| |jwks|
|**jwksUri**|String|False| |jwksUri|
|**logoUri**|String|False| |logoUri|
|**multiTenant**|Boolean|False| |multiTenant|
|**policyUri**|String|False| |policyUri|
|**redirectUris**|String|False| |redirectUris|
|**refreshTokenValiditySeconds**|Integer|False| |refreshTokenValiditySeconds|
|**scope**|String|False| |scope|
|**secret**|String|False| |secret|
|**tokenEndpointAuthMethod**|String|False| |tokenEndpointAuthMethod|
|**tosUri**|String|False| |tosUri|
|**userType**|String|False| |userType|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result|更新后返回app|

### Result
|名称|类型|描述|
|---|---|---|
|**accessTokenValiditySeconds**|Integer|accessTokenValiditySeconds|
|**account**|String|account|
|**clientId**|String|应用ID|
|**clientName**|String|应用名|
|**clientUri**|String|clientUri|
|**contacts**|String|contacts|
|**createTime**|Integer|createTime|
|**extension**|String|extension|
|**grantTypes**|String|grantTypes|
|**jwks**|String|jwks|
|**jwksUri**|String|jwksUri|
|**logoUri**|String|logoUri|
|**multiTenant**|Boolean|multiTenant|
|**policyUri**|String|policyUri|
|**redirectUris**|String|redirectUris|
|**refreshTokenValiditySeconds**|Integer|refreshTokenValiditySeconds|
|**responseTypes**|String|responseTypes|
|**scope**|String|scope|
|**secretUpdateTime**|Integer|secretUpdateTime|
|**tokenEndpointAuthMethod**|String|tokenEndpointAuthMethod|
|**tosUri**|String|tosUri|
|**updateTime**|Integer|updateTime|
|**userType**|String|userType|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
