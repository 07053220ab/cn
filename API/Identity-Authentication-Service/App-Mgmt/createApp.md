## 描述
创建应用

## 限制
每个账户下支持创建最多20个应用

## 请求方式
POST

## 请求地址
https://ias.jdcloud-api.com/v1/regions/{regionId}/app

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域编码，参考《公共说明》|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**clientName**|String|True| |应用名|
|**redirectUris**|String|True| |回调地址，最多4个，多个url之间用逗号,分隔，每个url长度不超过1000，url不支持#符号|
|**grantTypes**|String|True| |支持的OAuth类型：<br>authorization_code：OAuth2授权码模式<br>implicit：OAuth2隐式授权模式<br>refresh_token：启用刷新令牌<br><br>grantTypes支持以下值：<br>（1）authorization_code<br>（2）authorization_code,refresh_token<br>（3）authorization_code,implicit<br>（4）authorization_code,implicit,refresh_token<br>（5）implicit<br><br>注：如果grantTypes指定了refresh_token，应用将可以使用刷新令牌；如果在创建应用时未指定，则应用不能使用刷新令牌；任何时候应用都可以调用“更新应用”接口更改grantTypes设置|
|**tokenEndpointAuthMethod**|String|True| |客户端认证方式：<br>none：不设置客户端密码（不推荐）<br>client_secret_post：客户端必须设置密码，且该密码需要在 OAuth2 Token Endpoint 提供于请求的 body<br>client_secret_basic：客户端必须设置密码，且该密码需要在 OAuth2 Token Endpoint 提供于请求的 header<br><br>支持以下值：<br>（1）none<br>（2）client_secret_post<br>（3）client_secret_basic|
|**accessTokenValiditySeconds**|Integer|True| |访问令牌有效期，值的范围为600到21,600，单位为秒，即10分钟到6小时|
|**contacts**|String|False| |contacts|
|**extension**|String|False| |extension|
|**jwks**|String|False| |jwks|
|**jwksUri**|String|False| |jwksUri|
|**logoUri**|String|False| |logoUri|
|**multiTenant**|Boolean|False| |multiTenant|
|**policyUri**|String|False| |policyUri|
|**clientUri**|String|False| |clientUri|
|**refreshTokenValiditySeconds**|Integer|False| |refreshTokenValiditySeconds|
|**scope**|String|False| |scope|
|**secret**|String|False| |secret|
|**tosUri**|String|False| |tosUri|
|**userType**|String|False| |userType|



## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String| |
|**result**|Result|创建app返回结果|

### Result
|名称|类型|描述|
|---|---|---|
|**accessTokenValiditySeconds**|Integer|accessTokenValiditySeconds|
|**account**|String|account|
|**clientId**|String|应用|
|**clientName**|String|应用名|
|**clientUri**|String|clientUri|
|**contacts**|String|contacts|
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
|**userType**|String|userType|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
