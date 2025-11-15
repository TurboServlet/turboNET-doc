# TurboNET Alpha api 文档

Nya~  
marked by 桃玖 & CtrlcvsNya & Kiwi  

Base URLs: https://api.sys-allnet.com  

Swagger3 version (instead of github markdown) : https://api.sys-allnet.com/swagger-ui/index.html

# Authentication

# 网页-其他

<a id="opIduserApi"></a>

## POST 用户

POST /web/user

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|requesterId|query|string| 是 |requesterId|
|body|body|[UserRequestVO](#schemauserrequestvo)| 否 |none|

> 返回示例

> 200 Response

```
{"isMe":true,"maimaiName":"string","turboName":"string","qqNumber":"string","avatar":"string","permission":"string","warningTimes":0,"warningMessage":"string","isBanned":true,"bannedMessage":"string","maiStatistics":{"echartsLine":"string","deluxRating":0,"serverRanking":0,"averageAccuracy":0.1,"maxCombo":0,"fullCombo":0,"allPerfect":0,"totalScores":0,"achievementCount":{"sssPlus":0,"sss":0,"ssPlus":0,"ss":0,"s":0,"splus":0}},"playActivity":{"heatmapPoints":"string","playCount":0,"playTime":0.1,"firstPlay":"string","lastPlay":"string","playVersion":"string"},"best35":[{"musicId":0,"level":0.1,"diff":0,"musicName":"string","scoreRank":"string","achievement":0.1,"score":0}],"best15":[{"musicId":0,"level":0.1,"diff":0,"musicName":"string","scoreRank":"string","achievement":0.1,"score":0}],"recentScores":[{"musicId":0,"level":0.1,"diff":0,"musicName":"string","scoreRank":"string","achievement":0.1,"score":0}]}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[UserResponseVO](#schemauserresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowServerRequestsApi"></a>

## GET 展示服务器请求统计

GET /web/showServerRequests

> 返回示例

> 200 Response

```
{"requestsCount":0,"cachedRequestsCount":0,"exceptionRequestsCount":0,"exceptionRequestsCachedCount":0,"exceptionRequestsRate":0.1,"exceptionRequestsCachedRate":0.1,"exceptionRequestsUnCachedRate":0.1,"zlibSkippedRequestsCount":0,"zlibSkippedRequestsBefore":0,"zlibSkippedRequestsRateThanBefore":0.1,"retryRequestsCount":0,"retryRequestsBefore":0,"retryRequestsRateThanBefore":0.1,"panicRequestsCount":0,"panicRequestsBefore":0,"panicRequestsRateThanBefore":0.1}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ServerRequestsResponseVO](#schemaserverrequestsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowNetworkStatusApi"></a>

## GET 查看网络状况

GET /web/showNetworkStatus

> 返回示例

> 200 Response

```
[{"arcadeName":"string","arcadeType":"TURBO","workingStatus":"WORKING","lastHeartbeatSecond":"string","heartbeatMap":["WORKING"]}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[NetworkStatusResponseVO](#schemanetworkstatusresponsevo)]|false|none||none|
|» arcadeName|string|true|none||机厅名称|
|» arcadeType|string|true|none||机厅类型|
|» workingStatus|string|true|none||当前状态|
|» lastHeartbeatSecond|string|true|none||最后心跳包|
|» heartbeatMap|[string]|true|none||心跳图|

#### 枚举值

|属性|值|
|---|---|
|arcadeType|TURBO|
|arcadeType|SPECIAL_TYPE_ONE|
|workingStatus|WORKING|
|workingStatus|WARNING|
|workingStatus|ERROR|
|workingStatus|UNKNOWN|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

<a id="opIdserverRequestsEchartsApi"></a>

## GET 展示服务器请求统计图

GET /web/serverRequestsEcharts

> 返回示例

> 200 Response

```
{"cachedLatency":[[0]],"unCachedLatency":[[0]],"startTimeStamp":0,"endTimeStamp":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ServerRequestsEchartsResponseVO](#schemaserverrequestsechartsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdrecordsApi"></a>

## GET 用户历史游玩记录

GET /web/records

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|page|query|Int| 是 |page|

> 返回示例

> 200 Response

```
{"content":[{"musicId":0,"musicName":"string","musicAuthor":"string","musicDiff":0,"musicLevel":0.1,"isDxMusic":true,"achievement":0.1,"isNewRecord":true,"addRating":0,"comboInfo":{"type":0,"combo":0,"maxCombo":0},"syncInfo":{"type":0,"sync":0,"maxSync":0},"score":{"critical":0,"perfect":0,"great":0,"good":0,"miss":0}}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTORecordsResponseVO](#schemapagedtorecordsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-设置相关

<a id="opIdsetUserSettingsApi"></a>

## POST 用户turbo设定

POST /web/setUserSettings

> Body 请求参数

```json
{
  "policyName": "string",
  "policy": "EVERYONE"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SetUserSettingsRequestVO](#schemasetusersettingsrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowUserSettingsApi"></a>

## GET 用户turbo设定

GET /web/showUserSettings

> 返回示例

> 200 Response

```
{"userPageAccessible":"EVERYONE","best35Accessible":"EVERYONE","best15Accessible":"EVERYONE","recentScoresAccessible":"EVERYONE"}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ShowUserSettingsResponseVO](#schemashowusersettingsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-舞萌相关-跑图券

<a id="opIdsetTicketsApi"></a>

## POST 设定跑图券

POST /web/setTickets

> Body 请求参数

```json
{
  "ticketId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SetTicketsRequestVO](#schemasetticketsrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdresetTicketsApi"></a>

## POST 取消设定跑图券

POST /web/resetTickets

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdcurrentTicketsApi"></a>

## GET 当前设定跑图券

GET /web/currentTickets

> 返回示例

> 200 Response

```
{"turboTicket":{"isEnable":true,"ticketId":0},"maimaiTickets":[{"ticketId":0,"stock":0}]}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[CurrentTicketsResponseVO](#schemacurrentticketsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-舞萌相关-maimai个性化设置

<a id="opIdsetMaimaiNameApi"></a>

## POST 设定maimai名称

POST /web/setMaimaiName

> Body 请求参数

```json
{
  "maimaiName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SetMaimaiNameRequestVO](#schemasetmaimainamerequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdsetAvatarApi"></a>

## POST 设定maimai头像

POST /web/setAvatar

> Body 请求参数

```json
{
  "avatarBase64": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SetAvatarRequestVO](#schemasetavatarrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdresetMaimaiNameApi"></a>

## POST 重置maimai名称

POST /web/resetMaimaiName

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdresetAvatarApi"></a>

## POST 重置maimai头像

POST /web/resetAvatar

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowMaimaiNameApi"></a>

## GET 展示maimai名称

GET /web/showMaimaiName

> 返回示例

> 200 Response

```
"string"
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-NET好友

<a id="opIdsetFriendSearchPolicyApi"></a>

## POST 设置好友查找权限

POST /web/setFriendSearchPolicy

> Body 请求参数

```json
{
  "policy": "AUTO_ACCEPT"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendSearchPolicyRequestVO](#schemafriendsearchpolicyrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdremoveRivalApi"></a>

## POST 删除对手

POST /web/removeRival

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdremoveFriendApi"></a>

## POST 移除好友

POST /web/removeFriend

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIddenyFriendApi"></a>

## POST 拒绝好友

POST /web/denyFriend

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdaddRivalApi"></a>

## POST 添加对手

POST /web/addRival

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdaddFriendApi"></a>

## POST 添加好友

POST /web/addFriend

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdacceptFriendApi"></a>

## POST 同意好友请求

POST /web/acceptFriend

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FriendRequestVO](#schemafriendrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowRivalApi"></a>

## GET 展示对手

GET /web/showRival

> 返回示例

> 200 Response

```
{"turboNameList":["string"],"length":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ShowRivalResponseVO](#schemashowrivalresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowFriendsApi"></a>

## GET 好友列表

GET /web/showFriends

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|page|query|Int| 是 |page|

> 返回示例

> 200 Response

```
{"content":[{"turboName":"string","avatar":"string","lastPlayHour":"string","lastPlayPlace":"string","permission":"ADMIN","warningTimes":0,"isBanned":true}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTOShowFriendsResponseVO](#schemapagedtoshowfriendsresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowFriendSearchPolicyApi"></a>

## GET 展示好友查找权限

GET /web/showFriendSearchPolicy

> 返回示例

> 200 Response

```
"AUTO_ACCEPT"
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowFriendRequestsApi"></a>

## GET 好友请求列表

GET /web/showFriendRequests

> 返回示例

> 200 Response

```
[{"turboName":"string","avatar":"string","permission":"ADMIN","warningTimes":0,"isBanned":true,"requestTime":"string"}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ShowFriendRequestsResponseVO](#schemashowfriendrequestsresponsevo)]|false|none||none|
|» turboName|string|true|none||turbo名称|
|» avatar|string|true|none||头像|
|» permission|string|true|none||权限|
|» warningTimes|integer(int32)|true|none||警告时间|
|» isBanned|boolean|true|none||是否封禁|
|» requestTime|string|true|none||请求时间|

#### 枚举值

|属性|值|
|---|---|
|permission|ADMIN|
|permission|BUILDER|
|permission|AUTHORIZER|
|permission|USER|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

# 网页-舞萌相关-相片

<a id="opIdremoveFavoriteApi"></a>

## POST 纪念图片取消喜欢

POST /web/removeFavorite

> Body 请求参数

```json
{
  "photoId": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FavoriteRequestVO](#schemafavoriterequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdaddFavoriteApi"></a>

## POST 纪念图片添加喜欢

POST /web/addFavorite

> Body 请求参数

```json
{
  "photoId": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[FavoriteRequestVO](#schemafavoriterequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdhistoryPhotosApi"></a>

## GET 用户turbo历史图片

GET /web/historyPhotos

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|page|query|Int| 是 |page|

> 返回示例

> 200 Response

```
{"content":[{"photoId":"string","isFavorite":true}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTOHistoryPhotosResponseVO](#schemapagedtohistoryphotosresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdfavoritePhotosApi"></a>

## GET 用户turbo历史喜爱图片

GET /web/favoritePhotos

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|page|query|Int| 是 |page|

> 返回示例

> 200 Response

```
{"content":["string"],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTOString](#schemapagedtostring)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-机厅信息

<a id="opIdremoveArcadeAliasApi"></a>

## POST 删除机厅别名
 注意本api仅管理员可用

POST /web/removeArcadeAlias

> Body 请求参数

```json
{
  "arcadeName": "string",
  "arcadeAlias": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[ArcadeAliasRequestVO](#schemaarcadealiasrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdsetArcadeSettingsApi"></a>

## POST 新增机厅别名
 注意本api仅管理员和技术管理员可用

POST /web/addArcadeAlias

> Body 请求参数

```json
{
  "arcadeName": "string",
  "arcadeAlias": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[ArcadeAliasRequestVO](#schemaarcadealiasrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowArcadeSettingsApi"></a>

## GET 展示机厅别名

GET /web/showArcadeAlias

> 返回示例

> 200 Response

```
{"permission":"ADMIN","arcadeList":[{"arcadeName":"string","arcadeType":"TURBO","arcadeAlias":["string"]}]}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ShowArcadeAliasResponseVO](#schemashowarcadealiasresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdarcadeInfoApi"></a>

## GET 去过的机厅信息

GET /web/arcadeInfo

> 返回示例

> 200 Response

```
[{"arcadeName":"string","arcadeType":"TURBO","arcadePlayCount":0,"arcadeRequested":0,"arcadeCachedRequest":0,"arcadeFixedRequest":0,"arcadeCachedHitRate":0.1,"singleArcadeInfo":[{"singleName":"string","isEnableCustomName":true,"isEnableCustomAvatar":true,"isEnableTurboTicket":true,"arcadeEnableSetting":["string"]}]}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ArcadeInfoResponseVO](#schemaarcadeinforesponsevo)]|false|none||none|
|» arcadeName|string|true|none||机厅名称|
|» arcadeType|string|true|none||机厅类型|
|» arcadePlayCount|integer(int32)|true|none||机厅pc数|
|» arcadeRequested|integer(int32)|true|none||机厅请求|
|» arcadeCachedRequest|integer(int32)|true|none||机厅缓存|
|» arcadeFixedRequest|integer(int32)|true|none||机厅修复|
|» arcadeCachedHitRate|number(double)|true|none||hitRate|
|» singleArcadeInfo|[[SingleArcadeInfo](#schemasinglearcadeinfo)]|true|none||单独机厅设置信息|
|»» singleName|string|true|none||单独机厅设置信息|
|»» isEnableCustomName|boolean|true|none||是否启用自定义名称|
|»» isEnableCustomAvatar|boolean|true|none||是否启用自定义头像|
|»» isEnableTurboTicket|boolean|true|none||是否使用跑图券|
|»» arcadeEnableSetting|[string]|true|none||是否启用自定义设置|

#### 枚举值

|属性|值|
|---|---|
|arcadeType|TURBO|
|arcadeType|SPECIAL_TYPE_ONE|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

<a id="opIdarcadeInfoDetailApi"></a>

## GET 去过的机厅详情

GET /web/arcadeInfoDetail

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|arcadeName|query|String| 是 |arcadeName|

> 返回示例

> 200 Response

```
{"arcadeInfo":{"arcadeName":"string","arcadeType":"TURBO","arcadePlayCount":0,"arcadeRequested":0,"arcadeCachedRequest":0,"arcadeFixedRequest":0,"arcadeCachedHitRate":0.1,"singleArcadeInfo":[{"singleName":"string","isEnableCustomName":true,"isEnableCustomAvatar":true,"isEnableTurboTicket":true,"arcadeEnableSetting":["string"]}]},"thirtyMinutesPlayer":0,"oneHourPlayer":0,"twoHoursPlayer":0,"thirtyMinutesPlayCount":0,"oneHourPlayCount":0,"twoHoursPlayCount":0,"playerList":[{"userIdHash":"string","maimaiName":"string","turboName":"string","isTurboAdmin":true,"playdate":"string"}],"thirtyMinutesPlayerList":[{"userIdHash":"string","maimaiName":"string","turboName":"string","isTurboAdmin":true,"playdate":"string"}]}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[ArcadeInfoDetailResponseVO](#schemaarcadeinfodetailresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# Bot相关Api

<a id="opIdunbindApi"></a>

## POST 解绑

POST /bot/unbind

> Body 请求参数

```json
{
  "token": "string",
  "botId": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[UnbindRequestVO](#schemaunbindrequestvo)| 否 |none|

> 返回示例

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdbindApi"></a>

## POST 绑定

POST /bot/bind

> Body 请求参数

```json
{
  "botName": "string",
  "botToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[Bot bind](#schemabot bind)| 否 |none|

> 返回示例

> 200 Response

```
{"botId":"string","botKey":"string"}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[bind response](#schemabind response)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-用户权限

<a id="opIdupgradeTurboPermissionListApi"></a>

## GET 用户turbo历史权限修改记录

GET /web/upgradeTurboPermissionList

> 返回示例

> 200 Response

```
[{"turboName":"string","permission":"string"}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[UpgradeTurboPermissionResponseVO](#schemaupgradeturbopermissionresponsevo)]|false|none||none|
|» turboName|string|true|none||turbo名称|
|» permission|string|true|none||权限|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

<a id="opIdturboPermissionApi"></a>

## GET 用户turbo权限

GET /web/turboPermission

> 返回示例

> 200 Response

```
{"turboName":"string","avatar":"string","permission":"string","warningTimes":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[TurboPermissionResponseVO](#schematurbopermissionresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdshowTurboPermissionApi"></a>

## GET 用户turbo权限可进行的操作

GET /web/showTurboPermission

> 返回示例

> 200 Response

```
[{"permissionDescription":"string","isGranted":true}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ShowTurboPermissionResponseVO](#schemashowturbopermissionresponsevo)]|false|none||none|
|» permissionDescription|string|true|none||权限描述|
|» isGranted|boolean|true|none||是否授予|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

<a id="opIdexecuteRecordListApi"></a>

## GET 用户turbo历史权限封禁记录

GET /web/executeRecordList

> 返回示例

> 200 Response

```
[{"recordId":"string","turboName":"string","type":"string","reason":"string"}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ExecuteRecordResponseVO](#schemaexecuterecordresponsevo)]|false|none||none|
|» recordId|string|true|none||记录id|
|» turboName|string|true|none||turbo名称|
|» type|string|true|none||类型|
|» reason|string|true|none||理由|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

# 网页-舞萌相关-QrCode

<a id="opIdshowQrCommandListApi"></a>

## GET 展示机台可操作的选项
注意
该部分功能较为高危，您在机台上应用的设置将作用于全部玩家，请谨慎使用。

GET /web/showQrCommandList

> 返回示例

> 200 Response

```
[{"functionType":"LOGIN","setting":"NONE"}]
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ShowQrCommandListResponseVO](#schemashowqrcommandlistresponsevo)]|false|none||none|
|» functionType|string|true|none||自定义类型|
|» setting|string|true|none||设置|

#### 枚举值

|属性|值|
|---|---|
|functionType|LOGIN|
|functionType|KASTANJ_LOGIN|
|functionType|SPECIAL_TYPE_ONE_LOGIN|
|functionType|SETTING|
|functionType|PING|
|setting|NONE|
|setting|MASK_USERNAME|
|setting|UDEMAE_SHOW_ACHIEVEMENT|
|setting|DISABLE_TICKET|
|setting|DISABLE_CUSTOM_NAME|
|setting|DISABLE_CUSTOM_AVATAR|

状态码 **400**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **401**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **403**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **410**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

状态码 **500**

*全局返回*

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» code|integer(int32)|true|none||返回码|
|» message|string|true|none||提示信息|

<a id="opIdgetQrCommandDataApi"></a>

## GET 获取机台操作的二维码
注意
该部分功能较为高危，您在机台上应用的设置将作用于全部玩家，请谨慎使用。

GET /web/getQrCommandData

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|functionType|query|string| 是 |none|
|setting|query|string| 是 |none|

#### 枚举值

|属性|值|
|---|---|
|functionType|LOGIN|
|functionType|KASTANJ_LOGIN|
|functionType|SPECIAL_TYPE_ONE_LOGIN|
|functionType|SETTING|
|functionType|PING|
|setting|NONE|
|setting|MASK_USERNAME|
|setting|UDEMAE_SHOW_ACHIEVEMENT|
|setting|DISABLE_TICKET|
|setting|DISABLE_CUSTOM_NAME|
|setting|DISABLE_CUSTOM_AVATAR|

> 返回示例

> 200 Response

```
{"qrData":"string","valid":"string"}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[GetQrCommandResponseVO](#schemagetqrcommandresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 网页-舞萌相关-排行榜

<a id="opIdmusicRankingApi"></a>

## GET 指定乐曲排行榜

GET /web/musicRanking

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|musicId|query|integer(int64)| 是 |none|
|musicDiff|query|integer(int32)| 是 |none|
|onlyTurbo|query|boolean| 是 |none|
|page|query|integer(int32)| 是 |none|

> 返回示例

> 200 Response

```
{"content":[{"ranking":0,"maimaiName":"string","turboName":"string","achievement":0.1,"deluxScore":0}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTOMusicRankingResponseVO](#schemapagedtomusicrankingresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIddxRatingRankingApi"></a>

## GET Dx分数排行榜

GET /web/dxRatingRanking

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|onlyTurbo|query|boolean| 是 |none|
|page|query|integer(int32)| 是 |none|

> 返回示例

> 200 Response

```
{"content":[{"ranking":0,"maimaiName":"string","turboName":"string","rating":0}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTODxRatingRankingResponseVO](#schemapagedtodxratingrankingresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

<a id="opIdachievementRankingApi"></a>

## GET Dx分数排行榜

GET /web/achievementRanking

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|onlyTurbo|query|boolean| 是 |none|
|page|query|integer(int32)| 是 |none|

> 返回示例

> 200 Response

```
{"content":[{"ranking":0,"maimaiName":"string","turboName":"string","achievement":0.1}],"totalElements":0,"totalPages":0}
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[PageDTOAchievementRankingResponseVO](#schemapagedtoachievementrankingresponsevo)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 权限相关

<a id="opIdshowPermission"></a>

## GET 展示用户权限

GET /permission/showPermission

> 返回示例

> 200 Response

```
"ADMIN"
```

> 400 Response

```json
{
  "code": 0,
  "message": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|captcha验证失败或者是不合法的数据|[Global exception](#schemaglobal exception)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请求的Token缺失或Token不合法，请检查|[Global exception](#schemaglobal exception)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|权限不足，请检查请求体的权限|[Global exception](#schemaglobal exception)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|该用户已被封禁，请联系管理员进行处理|[Global exception](#schemaglobal exception)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|我抄，服务器出现内部错误了，怎么会这样|[Global exception](#schemaglobal exception)|

# 数据模型

<h2 id="tocS_UserRequestVO">UserRequestVO</h2>

<a id="schemauserrequestvo"></a>
<a id="schema_UserRequestVO"></a>
<a id="tocSuserrequestvo"></a>
<a id="tocsuserrequestvo"></a>

```json
{
  "turboName": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||none|

<h2 id="tocS_Global exception">Global exception</h2>

<a id="schemaglobal exception"></a>
<a id="schema_Global exception"></a>
<a id="tocSglobal exception"></a>
<a id="tocsglobal exception"></a>

```json
{
  "code": 0,
  "message": "string"
}

```

全局返回

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|true|none||返回码|
|message|string|true|none||提示信息|

<h2 id="tocS_AchievementCount">AchievementCount</h2>

<a id="schemaachievementcount"></a>
<a id="schema_AchievementCount"></a>
<a id="tocSachievementcount"></a>
<a id="tocsachievementcount"></a>

```json
{
  "sssPlus": 0,
  "sss": 0,
  "ssPlus": 0,
  "ss": 0,
  "sPlus": 0,
  "s": 0,
  "splus": 0
}

```

总成绩

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|sssPlus|integer(int32)|true|none||none|
|sss|integer(int32)|true|none||none|
|ssPlus|integer(int32)|true|none||none|
|ss|integer(int32)|true|none||none|
|sPlus|integer(int32)|false|write-only||none|
|s|integer(int32)|true|none||none|
|splus|integer(int32)|true|none||none|

<h2 id="tocS_MaiStatistics">MaiStatistics</h2>

<a id="schemamaistatistics"></a>
<a id="schema_MaiStatistics"></a>
<a id="tocSmaistatistics"></a>
<a id="tocsmaistatistics"></a>

```json
{
  "echartsLine": "string",
  "deluxRating": 0,
  "serverRanking": 0,
  "averageAccuracy": 0.1,
  "maxCombo": 0,
  "fullCombo": 0,
  "allPerfect": 0,
  "totalScores": 0,
  "achievementCount": {
    "sssPlus": 0,
    "sss": 0,
    "ssPlus": 0,
    "ss": 0,
    "sPlus": 0,
    "s": 0,
    "splus": 0
  }
}

```

maimai状态

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|echartsLine|string|true|none||数据可视化|
|deluxRating|integer(int32)|true|none||DX分数|
|serverRanking|integer(int32)|true|none||服务器排名|
|averageAccuracy|number(double)|true|none||平均达成率|
|maxCombo|integer(int32)|true|none||最大连击数|
|fullCombo|integer(int32)|true|none||fullCombo|
|allPerfect|integer(int32)|true|none||allPerfect|
|totalScores|integer(int64)|true|none||总分数|
|achievementCount|[AchievementCount](#schemaachievementcount)|true|none||总成绩|

<h2 id="tocS_MusicInfo">MusicInfo</h2>

<a id="schemamusicinfo"></a>
<a id="schema_MusicInfo"></a>
<a id="tocSmusicinfo"></a>
<a id="tocsmusicinfo"></a>

```json
{
  "musicId": 0,
  "level": 0.1,
  "diff": 0,
  "musicName": "string",
  "scoreRank": "string",
  "achievement": 0.1,
  "score": 0
}

```

当前分数

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|musicId|integer(int32)|true|none||none|
|level|number(double)|true|none||none|
|diff|integer(int32)|true|none||none|
|musicName|string|true|none||none|
|scoreRank|string|true|none||none|
|achievement|number(double)|true|none||none|
|score|integer(int32)|true|none||none|

<h2 id="tocS_PlayActivity">PlayActivity</h2>

<a id="schemaplayactivity"></a>
<a id="schema_PlayActivity"></a>
<a id="tocSplayactivity"></a>
<a id="tocsplayactivity"></a>

```json
{
  "heatmapPoints": "string",
  "playCount": 0,
  "playTime": 0.1,
  "firstPlay": "string",
  "lastPlay": "string",
  "playVersion": "string"
}

```

游玩时间

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|heatmapPoints|string|true|none||none|
|playCount|integer(int32)|true|none||none|
|playTime|number(double)|true|none||none|
|firstPlay|string|true|none||none|
|lastPlay|string|true|none||none|
|playVersion|string|true|none||none|

<h2 id="tocS_UserResponseVO">UserResponseVO</h2>

<a id="schemauserresponsevo"></a>
<a id="schema_UserResponseVO"></a>
<a id="tocSuserresponsevo"></a>
<a id="tocsuserresponsevo"></a>

```json
{
  "isMe": true,
  "maimaiName": "string",
  "turboName": "string",
  "qqNumber": "string",
  "avatar": "string",
  "permission": "string",
  "warningTimes": 0,
  "warningMessage": "string",
  "isBanned": true,
  "bannedMessage": "string",
  "maiStatistics": {
    "echartsLine": "string",
    "deluxRating": 0,
    "serverRanking": 0,
    "averageAccuracy": 0.1,
    "maxCombo": 0,
    "fullCombo": 0,
    "allPerfect": 0,
    "totalScores": 0,
    "achievementCount": {
      "sssPlus": 0,
      "sss": 0,
      "ssPlus": 0,
      "ss": 0,
      "sPlus": 0,
      "s": 0,
      "splus": 0
    }
  },
  "playActivity": {
    "heatmapPoints": "string",
    "playCount": 0,
    "playTime": 0.1,
    "firstPlay": "string",
    "lastPlay": "string",
    "playVersion": "string"
  },
  "best35": [
    {
      "musicId": 0,
      "level": 0.1,
      "diff": 0,
      "musicName": "string",
      "scoreRank": "string",
      "achievement": 0.1,
      "score": 0
    }
  ],
  "best15": [
    {
      "musicId": 0,
      "level": 0.1,
      "diff": 0,
      "musicName": "string",
      "scoreRank": "string",
      "achievement": 0.1,
      "score": 0
    }
  ],
  "recentScores": [
    {
      "musicId": 0,
      "level": 0.1,
      "diff": 0,
      "musicName": "string",
      "scoreRank": "string",
      "achievement": 0.1,
      "score": 0
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isMe|boolean|true|none||是我？|
|maimaiName|string|true|none||maimai名称|
|turboName|string|true|none||turbo名称|
|qqNumber|string|true|none||QQ号|
|avatar|string|true|none||头像|
|permission|string|true|none||权限|
|warningTimes|integer(int32)|true|none||警告时间|
|warningMessage|string|true|none||警告信息|
|isBanned|boolean|true|none||是否封禁|
|bannedMessage|string|true|none||封禁理由|
|maiStatistics|[MaiStatistics](#schemamaistatistics)|true|none||maimai状态|
|playActivity|[PlayActivity](#schemaplayactivity)|true|none||游玩时间|
|best35|[[MusicInfo](#schemamusicinfo)]|true|none||b35|
|best15|[[MusicInfo](#schemamusicinfo)]|true|none||b15|
|recentScores|[[MusicInfo](#schemamusicinfo)]|true|none||当前分数|

<h2 id="tocS_SetUserSettingsRequestVO">SetUserSettingsRequestVO</h2>

<a id="schemasetusersettingsrequestvo"></a>
<a id="schema_SetUserSettingsRequestVO"></a>
<a id="tocSsetusersettingsrequestvo"></a>
<a id="tocssetusersettingsrequestvo"></a>

```json
{
  "policyName": "string",
  "policy": "EVERYONE"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|policyName|string|true|none||none|
|policy|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|policy|EVERYONE|
|policy|ONLY_FRIENDS|
|policy|ONLY_ME|

<h2 id="tocS_SetTicketsRequestVO">SetTicketsRequestVO</h2>

<a id="schemasetticketsrequestvo"></a>
<a id="schema_SetTicketsRequestVO"></a>
<a id="tocSsetticketsrequestvo"></a>
<a id="tocssetticketsrequestvo"></a>

```json
{
  "ticketId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||none|

<h2 id="tocS_SetMaimaiNameRequestVO">SetMaimaiNameRequestVO</h2>

<a id="schemasetmaimainamerequestvo"></a>
<a id="schema_SetMaimaiNameRequestVO"></a>
<a id="tocSsetmaimainamerequestvo"></a>
<a id="tocssetmaimainamerequestvo"></a>

```json
{
  "maimaiName": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|maimaiName|string|true|none||none|

<h2 id="tocS_FriendSearchPolicyRequestVO">FriendSearchPolicyRequestVO</h2>

<a id="schemafriendsearchpolicyrequestvo"></a>
<a id="schema_FriendSearchPolicyRequestVO"></a>
<a id="tocSfriendsearchpolicyrequestvo"></a>
<a id="tocsfriendsearchpolicyrequestvo"></a>

```json
{
  "policy": "AUTO_ACCEPT"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|policy|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|policy|AUTO_ACCEPT|
|policy|MANUAL|
|policy|FRIENDS_OF_FRIENDS|
|policy|NOBODY|

<h2 id="tocS_SetAvatarRequestVO">SetAvatarRequestVO</h2>

<a id="schemasetavatarrequestvo"></a>
<a id="schema_SetAvatarRequestVO"></a>
<a id="tocSsetavatarrequestvo"></a>
<a id="tocssetavatarrequestvo"></a>

```json
{
  "avatarBase64": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|avatarBase64|string|true|none||none|

<h2 id="tocS_FriendRequestVO">FriendRequestVO</h2>

<a id="schemafriendrequestvo"></a>
<a id="schema_FriendRequestVO"></a>
<a id="tocSfriendrequestvo"></a>
<a id="tocsfriendrequestvo"></a>

```json
{
  "turboName": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||turbo名称|

<h2 id="tocS_FavoriteRequestVO">FavoriteRequestVO</h2>

<a id="schemafavoriterequestvo"></a>
<a id="schema_FavoriteRequestVO"></a>
<a id="tocSfavoriterequestvo"></a>
<a id="tocsfavoriterequestvo"></a>

```json
{
  "photoId": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoId|string|true|none||none|

<h2 id="tocS_ArcadeAliasRequestVO">ArcadeAliasRequestVO</h2>

<a id="schemaarcadealiasrequestvo"></a>
<a id="schema_ArcadeAliasRequestVO"></a>
<a id="tocSarcadealiasrequestvo"></a>
<a id="tocsarcadealiasrequestvo"></a>

```json
{
  "arcadeName": "string",
  "arcadeAlias": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|arcadeName|string|true|none||none|
|arcadeAlias|string|true|none||none|

<h2 id="tocS_UnbindRequestVO">UnbindRequestVO</h2>

<a id="schemaunbindrequestvo"></a>
<a id="schema_UnbindRequestVO"></a>
<a id="tocSunbindrequestvo"></a>
<a id="tocsunbindrequestvo"></a>

```json
{
  "token": "string",
  "botId": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|botId|string|true|none||none|

<h2 id="tocS_Bot bind">Bot bind</h2>

<a id="schemabot bind"></a>
<a id="schema_Bot bind"></a>
<a id="tocSbot bind"></a>
<a id="tocsbot bind"></a>

```json
{
  "botName": "string",
  "botToken": "string"
}

```

bot绑定

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botName|string|true|none||bot名称|
|botToken|string|true|none||Bot Token|

<h2 id="tocS_bind response">bind response</h2>

<a id="schemabind response"></a>
<a id="schema_bind response"></a>
<a id="tocSbind response"></a>
<a id="tocsbind response"></a>

```json
{
  "botId": "string",
  "botKey": "string"
}

```

bot绑定返回

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botId|string|true|none||Bot 名称|
|botKey|string|true|none||Bot 绑定密钥|

<h2 id="tocS_UpgradeTurboPermissionResponseVO">UpgradeTurboPermissionResponseVO</h2>

<a id="schemaupgradeturbopermissionresponsevo"></a>
<a id="schema_UpgradeTurboPermissionResponseVO"></a>
<a id="tocSupgradeturbopermissionresponsevo"></a>
<a id="tocsupgradeturbopermissionresponsevo"></a>

```json
{
  "turboName": "string",
  "permission": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||turbo名称|
|permission|string|true|none||权限|

<h2 id="tocS_TurboPermissionResponseVO">TurboPermissionResponseVO</h2>

<a id="schematurbopermissionresponsevo"></a>
<a id="schema_TurboPermissionResponseVO"></a>
<a id="tocSturbopermissionresponsevo"></a>
<a id="tocsturbopermissionresponsevo"></a>

```json
{
  "turboName": "string",
  "avatar": "string",
  "permission": "string",
  "warningTimes": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||turbo名称|
|avatar|string|true|none||头像|
|permission|string|true|none||权限|
|warningTimes|integer(int32)|true|none||警告时间|

<h2 id="tocS_ShowUserSettingsResponseVO">ShowUserSettingsResponseVO</h2>

<a id="schemashowusersettingsresponsevo"></a>
<a id="schema_ShowUserSettingsResponseVO"></a>
<a id="tocSshowusersettingsresponsevo"></a>
<a id="tocsshowusersettingsresponsevo"></a>

```json
{
  "userPageAccessible": "EVERYONE",
  "best35Accessible": "EVERYONE",
  "best15Accessible": "EVERYONE",
  "recentScoresAccessible": "EVERYONE"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|userPageAccessible|string|true|none||用户界面可见|
|best35Accessible|string|true|none||b35可见|
|best15Accessible|string|true|none||b15可见|
|recentScoresAccessible|string|true|none||最新成绩可见|

#### 枚举值

|属性|值|
|---|---|
|userPageAccessible|EVERYONE|
|userPageAccessible|ONLY_FRIENDS|
|userPageAccessible|ONLY_ME|
|best35Accessible|EVERYONE|
|best35Accessible|ONLY_FRIENDS|
|best35Accessible|ONLY_ME|
|best15Accessible|EVERYONE|
|best15Accessible|ONLY_FRIENDS|
|best15Accessible|ONLY_ME|
|recentScoresAccessible|EVERYONE|
|recentScoresAccessible|ONLY_FRIENDS|
|recentScoresAccessible|ONLY_ME|

<h2 id="tocS_ShowTurboPermissionResponseVO">ShowTurboPermissionResponseVO</h2>

<a id="schemashowturbopermissionresponsevo"></a>
<a id="schema_ShowTurboPermissionResponseVO"></a>
<a id="tocSshowturbopermissionresponsevo"></a>
<a id="tocsshowturbopermissionresponsevo"></a>

```json
{
  "permissionDescription": "string",
  "isGranted": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|permissionDescription|string|true|none||权限描述|
|isGranted|boolean|true|none||是否授予|

<h2 id="tocS_ServerRequestsResponseVO">ServerRequestsResponseVO</h2>

<a id="schemaserverrequestsresponsevo"></a>
<a id="schema_ServerRequestsResponseVO"></a>
<a id="tocSserverrequestsresponsevo"></a>
<a id="tocsserverrequestsresponsevo"></a>

```json
{
  "requestsCount": 0,
  "cachedRequestsCount": 0,
  "exceptionRequestsCount": 0,
  "exceptionRequestsCachedCount": 0,
  "exceptionRequestsRate": 0.1,
  "exceptionRequestsCachedRate": 0.1,
  "exceptionRequestsUnCachedRate": 0.1,
  "zlibSkippedRequestsCount": 0,
  "zlibSkippedRequestsBefore": 0,
  "zlibSkippedRequestsRateThanBefore": 0.1,
  "retryRequestsCount": 0,
  "retryRequestsBefore": 0,
  "retryRequestsRateThanBefore": 0.1,
  "panicRequestsCount": 0,
  "panicRequestsBefore": 0,
  "panicRequestsRateThanBefore": 0.1
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|requestsCount|integer(int32)|true|none||请求次数|
|cachedRequestsCount|integer(int32)|true|none||缓存请求次数|
|exceptionRequestsCount|integer(int32)|true|none||异常请求次数|
|exceptionRequestsCachedCount|integer(int32)|true|none||异常请求缓存次数|
|exceptionRequestsRate|number(double)|true|none||异常请求率|
|exceptionRequestsCachedRate|number(double)|true|none||异常请求缓存率|
|exceptionRequestsUnCachedRate|number(double)|true|none||异常请求未缓存率|
|zlibSkippedRequestsCount|integer(int32)|true|none||zlib跳过次数|
|zlibSkippedRequestsBefore|integer(int32)|true|none||zlib之前跳过次数|
|zlibSkippedRequestsRateThanBefore|number(double)|true|none||zlib相比之前跳过次数|
|retryRequestsCount|integer(int32)|true|none||重试请求次数|
|retryRequestsBefore|integer(int32)|true|none||之前重试请求次数|
|retryRequestsRateThanBefore|number(double)|true|none||相比之前重试请求次数|
|panicRequestsCount|integer(int32)|true|none||panicRequestsCount|
|panicRequestsBefore|integer(int32)|true|none||panicRequestsBefore|
|panicRequestsRateThanBefore|number(double)|true|none||panicRequestsRateThanBefore|

<h2 id="tocS_ShowRivalResponseVO">ShowRivalResponseVO</h2>

<a id="schemashowrivalresponsevo"></a>
<a id="schema_ShowRivalResponseVO"></a>
<a id="tocSshowrivalresponsevo"></a>
<a id="tocsshowrivalresponsevo"></a>

```json
{
  "turboNameList": [
    "string"
  ],
  "length": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboNameList|[string]|true|none||none|
|length|integer(int32)|true|none||none|

<h2 id="tocS_ShowQrCommandListResponseVO">ShowQrCommandListResponseVO</h2>

<a id="schemashowqrcommandlistresponsevo"></a>
<a id="schema_ShowQrCommandListResponseVO"></a>
<a id="tocSshowqrcommandlistresponsevo"></a>
<a id="tocsshowqrcommandlistresponsevo"></a>

```json
{
  "functionType": "LOGIN",
  "setting": "NONE"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|functionType|string|true|none||自定义类型|
|setting|string|true|none||设置|

#### 枚举值

|属性|值|
|---|---|
|functionType|LOGIN|
|functionType|KASTANJ_LOGIN|
|functionType|SPECIAL_TYPE_ONE_LOGIN|
|functionType|SETTING|
|functionType|PING|
|setting|NONE|
|setting|MASK_USERNAME|
|setting|UDEMAE_SHOW_ACHIEVEMENT|
|setting|DISABLE_TICKET|
|setting|DISABLE_CUSTOM_NAME|
|setting|DISABLE_CUSTOM_AVATAR|

<h2 id="tocS_NetworkStatusResponseVO">NetworkStatusResponseVO</h2>

<a id="schemanetworkstatusresponsevo"></a>
<a id="schema_NetworkStatusResponseVO"></a>
<a id="tocSnetworkstatusresponsevo"></a>
<a id="tocsnetworkstatusresponsevo"></a>

```json
{
  "arcadeName": "string",
  "arcadeType": "TURBO",
  "workingStatus": "WORKING",
  "lastHeartbeatSecond": "string",
  "heartbeatMap": [
    "WORKING"
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|arcadeName|string|true|none||机厅名称|
|arcadeType|string|true|none||机厅类型|
|workingStatus|string|true|none||当前状态|
|lastHeartbeatSecond|string|true|none||最后心跳包|
|heartbeatMap|[string]|true|none||心跳图|

#### 枚举值

|属性|值|
|---|---|
|arcadeType|TURBO|
|arcadeType|SPECIAL_TYPE_ONE|
|workingStatus|WORKING|
|workingStatus|WARNING|
|workingStatus|ERROR|
|workingStatus|UNKNOWN|

<h2 id="tocS_PageDTOShowFriendsResponseVO">PageDTOShowFriendsResponseVO</h2>

<a id="schemapagedtoshowfriendsresponsevo"></a>
<a id="schema_PageDTOShowFriendsResponseVO"></a>
<a id="tocSpagedtoshowfriendsresponsevo"></a>
<a id="tocspagedtoshowfriendsresponsevo"></a>

```json
{
  "content": [
    {
      "turboName": "string",
      "avatar": "string",
      "lastPlayHour": "string",
      "lastPlayPlace": "string",
      "permission": "ADMIN",
      "warningTimes": 0,
      "isBanned": true
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[ShowFriendsResponseVO](#schemashowfriendsresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_ShowFriendsResponseVO">ShowFriendsResponseVO</h2>

<a id="schemashowfriendsresponsevo"></a>
<a id="schema_ShowFriendsResponseVO"></a>
<a id="tocSshowfriendsresponsevo"></a>
<a id="tocsshowfriendsresponsevo"></a>

```json
{
  "turboName": "string",
  "avatar": "string",
  "lastPlayHour": "string",
  "lastPlayPlace": "string",
  "permission": "ADMIN",
  "warningTimes": 0,
  "isBanned": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||turbo名称|
|avatar|string|true|none||头像|
|lastPlayHour|string|true|none||距离上次游玩小时|
|lastPlayPlace|string|true|none||上次游玩地点|
|permission|string|true|none||权限|
|warningTimes|integer(int32)|true|none||警告时间|
|isBanned|boolean|true|none||是否封禁|

#### 枚举值

|属性|值|
|---|---|
|permission|ADMIN|
|permission|BUILDER|
|permission|AUTHORIZER|
|permission|USER|

<h2 id="tocS_ShowFriendRequestsResponseVO">ShowFriendRequestsResponseVO</h2>

<a id="schemashowfriendrequestsresponsevo"></a>
<a id="schema_ShowFriendRequestsResponseVO"></a>
<a id="tocSshowfriendrequestsresponsevo"></a>
<a id="tocsshowfriendrequestsresponsevo"></a>

```json
{
  "turboName": "string",
  "avatar": "string",
  "permission": "ADMIN",
  "warningTimes": 0,
  "isBanned": true,
  "requestTime": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||turbo名称|
|avatar|string|true|none||头像|
|permission|string|true|none||权限|
|warningTimes|integer(int32)|true|none||警告时间|
|isBanned|boolean|true|none||是否封禁|
|requestTime|string|true|none||请求时间|

#### 枚举值

|属性|值|
|---|---|
|permission|ADMIN|
|permission|BUILDER|
|permission|AUTHORIZER|
|permission|USER|

<h2 id="tocS_ArcadeList">ArcadeList</h2>

<a id="schemaarcadelist"></a>
<a id="schema_ArcadeList"></a>
<a id="tocSarcadelist"></a>
<a id="tocsarcadelist"></a>

```json
{
  "arcadeName": "string",
  "arcadeType": "TURBO",
  "arcadeAlias": [
    "string"
  ]
}

```

机厅列表

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|arcadeName|string|true|none||机厅名称|
|arcadeType|string|true|none||机厅类型|
|arcadeAlias|[string]|true|none||机厅别名|

#### 枚举值

|属性|值|
|---|---|
|arcadeType|TURBO|
|arcadeType|SPECIAL_TYPE_ONE|

<h2 id="tocS_ShowArcadeAliasResponseVO">ShowArcadeAliasResponseVO</h2>

<a id="schemashowarcadealiasresponsevo"></a>
<a id="schema_ShowArcadeAliasResponseVO"></a>
<a id="tocSshowarcadealiasresponsevo"></a>
<a id="tocsshowarcadealiasresponsevo"></a>

```json
{
  "permission": "ADMIN",
  "arcadeList": [
    {
      "arcadeName": "string",
      "arcadeType": "TURBO",
      "arcadeAlias": [
        "string"
      ]
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|permission|string|true|none||权限等级|
|arcadeList|[[ArcadeList](#schemaarcadelist)]|true|none||机厅列表|

#### 枚举值

|属性|值|
|---|---|
|permission|ADMIN|
|permission|BUILDER|
|permission|AUTHORIZER|
|permission|USER|

<h2 id="tocS_ServerRequestsEchartsResponseVO">ServerRequestsEchartsResponseVO</h2>

<a id="schemaserverrequestsechartsresponsevo"></a>
<a id="schema_ServerRequestsEchartsResponseVO"></a>
<a id="tocSserverrequestsechartsresponsevo"></a>
<a id="tocsserverrequestsechartsresponsevo"></a>

```json
{
  "cachedLatency": [
    [
      0
    ]
  ],
  "unCachedLatency": [
    [
      0
    ]
  ],
  "startTimeStamp": 0,
  "endTimeStamp": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|cachedLatency|[array]|true|none||已缓存|
|unCachedLatency|[array]|true|none||未缓存|
|startTimeStamp|integer(int64)|true|none||开始时间|
|endTimeStamp|integer(int64)|true|none||结束时间|

<h2 id="tocS_ComboInfo">ComboInfo</h2>

<a id="schemacomboinfo"></a>
<a id="schema_ComboInfo"></a>
<a id="tocScomboinfo"></a>
<a id="tocscomboinfo"></a>

```json
{
  "type": 0,
  "combo": 0,
  "maxCombo": 0
}

```

连击信息

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|type|integer(int32)|true|none||类型|
|combo|integer(int32)|true|none||连击数量|
|maxCombo|integer(int32)|true|none||最大连击|

<h2 id="tocS_PageDTORecordsResponseVO">PageDTORecordsResponseVO</h2>

<a id="schemapagedtorecordsresponsevo"></a>
<a id="schema_PageDTORecordsResponseVO"></a>
<a id="tocSpagedtorecordsresponsevo"></a>
<a id="tocspagedtorecordsresponsevo"></a>

```json
{
  "content": [
    {
      "musicId": 0,
      "musicName": "string",
      "musicAuthor": "string",
      "musicDiff": 0,
      "musicLevel": 0.1,
      "isDxMusic": true,
      "achievement": 0.1,
      "isNewRecord": true,
      "addRating": 0,
      "comboInfo": {
        "type": 0,
        "combo": 0,
        "maxCombo": 0
      },
      "syncInfo": {
        "type": 0,
        "sync": 0,
        "maxSync": 0
      },
      "score": {
        "critical": 0,
        "perfect": 0,
        "great": 0,
        "good": 0,
        "miss": 0
      }
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[RecordsResponseVO](#schemarecordsresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_RecordsResponseVO">RecordsResponseVO</h2>

<a id="schemarecordsresponsevo"></a>
<a id="schema_RecordsResponseVO"></a>
<a id="tocSrecordsresponsevo"></a>
<a id="tocsrecordsresponsevo"></a>

```json
{
  "musicId": 0,
  "musicName": "string",
  "musicAuthor": "string",
  "musicDiff": 0,
  "musicLevel": 0.1,
  "isDxMusic": true,
  "achievement": 0.1,
  "isNewRecord": true,
  "addRating": 0,
  "comboInfo": {
    "type": 0,
    "combo": 0,
    "maxCombo": 0
  },
  "syncInfo": {
    "type": 0,
    "sync": 0,
    "maxSync": 0
  },
  "score": {
    "critical": 0,
    "perfect": 0,
    "great": 0,
    "good": 0,
    "miss": 0
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|musicId|integer(int32)|true|none||乐曲id|
|musicName|string|true|none||乐曲名称|
|musicAuthor|string|true|none||乐曲作者|
|musicDiff|integer(int32)|true|none||乐曲难度|
|musicLevel|number(double)|true|none||乐曲等级|
|isDxMusic|boolean|true|none||是否DX谱面|
|achievement|number(double)|true|none||达成分数|
|isNewRecord|boolean|true|none||是否新纪录|
|addRating|integer(int32)|true|none||新增rating|
|comboInfo|[ComboInfo](#schemacomboinfo)|true|none||连击信息|
|syncInfo|[SyncInfo](#schemasyncinfo)|true|none||同步信息|
|score|[Score](#schemascore)|true|none||分数|

<h2 id="tocS_Score">Score</h2>

<a id="schemascore"></a>
<a id="schema_Score"></a>
<a id="tocSscore"></a>
<a id="tocsscore"></a>

```json
{
  "critical": 0,
  "perfect": 0,
  "great": 0,
  "good": 0,
  "miss": 0
}

```

分数

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|critical|integer(int32)|true|none||critical|
|perfect|integer(int32)|true|none||perfect|
|great|integer(int32)|true|none||great|
|good|integer(int32)|true|none||good|
|miss|integer(int32)|true|none||miss|

<h2 id="tocS_SyncInfo">SyncInfo</h2>

<a id="schemasyncinfo"></a>
<a id="schema_SyncInfo"></a>
<a id="tocSsyncinfo"></a>
<a id="tocssyncinfo"></a>

```json
{
  "type": 0,
  "sync": 0,
  "maxSync": 0
}

```

同步信息

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|type|integer(int32)|true|none||类型|
|sync|integer(int32)|true|none||同步分数|
|maxSync|integer(int32)|true|none||最大同步分数|

<h2 id="tocS_MusicRankingResponseVO">MusicRankingResponseVO</h2>

<a id="schemamusicrankingresponsevo"></a>
<a id="schema_MusicRankingResponseVO"></a>
<a id="tocSmusicrankingresponsevo"></a>
<a id="tocsmusicrankingresponsevo"></a>

```json
{
  "ranking": 0,
  "maimaiName": "string",
  "turboName": "string",
  "achievement": 0.1,
  "deluxScore": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ranking|integer(int32)|true|none||排名|
|maimaiName|string|true|none||maimai名称|
|turboName|string|true|none||turbo名称|
|achievement|number(double)|true|none||达成分数|
|deluxScore|integer(int32)|true|none||DX分数|

<h2 id="tocS_PageDTOMusicRankingResponseVO">PageDTOMusicRankingResponseVO</h2>

<a id="schemapagedtomusicrankingresponsevo"></a>
<a id="schema_PageDTOMusicRankingResponseVO"></a>
<a id="tocSpagedtomusicrankingresponsevo"></a>
<a id="tocspagedtomusicrankingresponsevo"></a>

```json
{
  "content": [
    {
      "ranking": 0,
      "maimaiName": "string",
      "turboName": "string",
      "achievement": 0.1,
      "deluxScore": 0
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[MusicRankingResponseVO](#schemamusicrankingresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_HistoryPhotosResponseVO">HistoryPhotosResponseVO</h2>

<a id="schemahistoryphotosresponsevo"></a>
<a id="schema_HistoryPhotosResponseVO"></a>
<a id="tocShistoryphotosresponsevo"></a>
<a id="tocshistoryphotosresponsevo"></a>

```json
{
  "photoId": "string",
  "isFavorite": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoId|string|true|none||相片id|
|isFavorite|boolean|true|none||是否为喜爱|

<h2 id="tocS_PageDTOHistoryPhotosResponseVO">PageDTOHistoryPhotosResponseVO</h2>

<a id="schemapagedtohistoryphotosresponsevo"></a>
<a id="schema_PageDTOHistoryPhotosResponseVO"></a>
<a id="tocSpagedtohistoryphotosresponsevo"></a>
<a id="tocspagedtohistoryphotosresponsevo"></a>

```json
{
  "content": [
    {
      "photoId": "string",
      "isFavorite": true
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[HistoryPhotosResponseVO](#schemahistoryphotosresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_GetQrCommandResponseVO">GetQrCommandResponseVO</h2>

<a id="schemagetqrcommandresponsevo"></a>
<a id="schema_GetQrCommandResponseVO"></a>
<a id="tocSgetqrcommandresponsevo"></a>
<a id="tocsgetqrcommandresponsevo"></a>

```json
{
  "qrData": "string",
  "valid": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|qrData|string|true|none||二维码数据|
|valid|string|true|none||有效期|

<h2 id="tocS_PageDTOString">PageDTOString</h2>

<a id="schemapagedtostring"></a>
<a id="schema_PageDTOString"></a>
<a id="tocSpagedtostring"></a>
<a id="tocspagedtostring"></a>

```json
{
  "content": [
    "string"
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[string]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_ExecuteRecordResponseVO">ExecuteRecordResponseVO</h2>

<a id="schemaexecuterecordresponsevo"></a>
<a id="schema_ExecuteRecordResponseVO"></a>
<a id="tocSexecuterecordresponsevo"></a>
<a id="tocsexecuterecordresponsevo"></a>

```json
{
  "recordId": "string",
  "turboName": "string",
  "type": "string",
  "reason": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|recordId|string|true|none||记录id|
|turboName|string|true|none||turbo名称|
|type|string|true|none||类型|
|reason|string|true|none||理由|

<h2 id="tocS_DxRatingRankingResponseVO">DxRatingRankingResponseVO</h2>

<a id="schemadxratingrankingresponsevo"></a>
<a id="schema_DxRatingRankingResponseVO"></a>
<a id="tocSdxratingrankingresponsevo"></a>
<a id="tocsdxratingrankingresponsevo"></a>

```json
{
  "ranking": 0,
  "maimaiName": "string",
  "turboName": "string",
  "rating": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ranking|integer(int32)|true|none||ranking|
|maimaiName|string|true|none||maimai名称|
|turboName|string|true|none||turbo名称|
|rating|integer(int32)|true|none||rating|

<h2 id="tocS_PageDTODxRatingRankingResponseVO">PageDTODxRatingRankingResponseVO</h2>

<a id="schemapagedtodxratingrankingresponsevo"></a>
<a id="schema_PageDTODxRatingRankingResponseVO"></a>
<a id="tocSpagedtodxratingrankingresponsevo"></a>
<a id="tocspagedtodxratingrankingresponsevo"></a>

```json
{
  "content": [
    {
      "ranking": 0,
      "maimaiName": "string",
      "turboName": "string",
      "rating": 0
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[DxRatingRankingResponseVO](#schemadxratingrankingresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

<h2 id="tocS_CurrentTicketsResponseVO">CurrentTicketsResponseVO</h2>

<a id="schemacurrentticketsresponsevo"></a>
<a id="schema_CurrentTicketsResponseVO"></a>
<a id="tocScurrentticketsresponsevo"></a>
<a id="tocscurrentticketsresponsevo"></a>

```json
{
  "turboTicket": {
    "isEnable": true,
    "ticketId": 0
  },
  "maimaiTickets": [
    {
      "ticketId": 0,
      "stock": 0
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboTicket|[TurboTicket](#schematurboticket)|true|none||turbo跑图券|
|maimaiTickets|[[MaimaiTickets](#schemamaimaitickets)]|true|none||maimai跑图券|

<h2 id="tocS_MaimaiTickets">MaimaiTickets</h2>

<a id="schemamaimaitickets"></a>
<a id="schema_MaimaiTickets"></a>
<a id="tocSmaimaitickets"></a>
<a id="tocsmaimaitickets"></a>

```json
{
  "ticketId": 0,
  "stock": 0
}

```

maimai跑图券

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||券id|
|stock|integer(int32)|true|none||数量|

<h2 id="tocS_TurboTicket">TurboTicket</h2>

<a id="schematurboticket"></a>
<a id="schema_TurboTicket"></a>
<a id="tocSturboticket"></a>
<a id="tocsturboticket"></a>

```json
{
  "isEnable": true,
  "ticketId": 0
}

```

turbo跑图券

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isEnable|boolean|true|none||是否启用|
|ticketId|integer(int32)|true|none||券id|

<h2 id="tocS_ArcadeInfoResponseVO">ArcadeInfoResponseVO</h2>

<a id="schemaarcadeinforesponsevo"></a>
<a id="schema_ArcadeInfoResponseVO"></a>
<a id="tocSarcadeinforesponsevo"></a>
<a id="tocsarcadeinforesponsevo"></a>

```json
{
  "arcadeName": "string",
  "arcadeType": "TURBO",
  "arcadePlayCount": 0,
  "arcadeRequested": 0,
  "arcadeCachedRequest": 0,
  "arcadeFixedRequest": 0,
  "arcadeCachedHitRate": 0.1,
  "singleArcadeInfo": [
    {
      "singleName": "string",
      "isEnableCustomName": true,
      "isEnableCustomAvatar": true,
      "isEnableTurboTicket": true,
      "arcadeEnableSetting": [
        "string"
      ]
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|arcadeName|string|true|none||机厅名称|
|arcadeType|string|true|none||机厅类型|
|arcadePlayCount|integer(int32)|true|none||机厅pc数|
|arcadeRequested|integer(int32)|true|none||机厅请求|
|arcadeCachedRequest|integer(int32)|true|none||机厅缓存|
|arcadeFixedRequest|integer(int32)|true|none||机厅修复|
|arcadeCachedHitRate|number(double)|true|none||hitRate|
|singleArcadeInfo|[[SingleArcadeInfo](#schemasinglearcadeinfo)]|true|none||单独机厅设置信息|

#### 枚举值

|属性|值|
|---|---|
|arcadeType|TURBO|
|arcadeType|SPECIAL_TYPE_ONE|

<h2 id="tocS_SingleArcadeInfo">SingleArcadeInfo</h2>

<a id="schemasinglearcadeinfo"></a>
<a id="schema_SingleArcadeInfo"></a>
<a id="tocSsinglearcadeinfo"></a>
<a id="tocssinglearcadeinfo"></a>

```json
{
  "singleName": "string",
  "isEnableCustomName": true,
  "isEnableCustomAvatar": true,
  "isEnableTurboTicket": true,
  "arcadeEnableSetting": [
    "string"
  ]
}

```

单独机厅设置信息

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|singleName|string|true|none||单独机厅设置信息|
|isEnableCustomName|boolean|true|none||是否启用自定义名称|
|isEnableCustomAvatar|boolean|true|none||是否启用自定义头像|
|isEnableTurboTicket|boolean|true|none||是否使用跑图券|
|arcadeEnableSetting|[string]|true|none||是否启用自定义设置|

<h2 id="tocS_ArcadeInfoDetailResponseVO">ArcadeInfoDetailResponseVO</h2>

<a id="schemaarcadeinfodetailresponsevo"></a>
<a id="schema_ArcadeInfoDetailResponseVO"></a>
<a id="tocSarcadeinfodetailresponsevo"></a>
<a id="tocsarcadeinfodetailresponsevo"></a>

```json
{
  "arcadeInfo": {
    "arcadeName": "string",
    "arcadeType": "TURBO",
    "arcadePlayCount": 0,
    "arcadeRequested": 0,
    "arcadeCachedRequest": 0,
    "arcadeFixedRequest": 0,
    "arcadeCachedHitRate": 0.1,
    "singleArcadeInfo": [
      {
        "singleName": "string",
        "isEnableCustomName": true,
        "isEnableCustomAvatar": true,
        "isEnableTurboTicket": true,
        "arcadeEnableSetting": [
          "string"
        ]
      }
    ]
  },
  "thirtyMinutesPlayer": 0,
  "oneHourPlayer": 0,
  "twoHoursPlayer": 0,
  "thirtyMinutesPlayCount": 0,
  "oneHourPlayCount": 0,
  "twoHoursPlayCount": 0,
  "playerList": [
    {
      "userIdHash": "string",
      "maimaiName": "string",
      "turboName": "string",
      "isTurboAdmin": true,
      "playdate": "string"
    }
  ],
  "thirtyMinutesPlayerList": [
    {
      "userIdHash": "string",
      "maimaiName": "string",
      "turboName": "string",
      "isTurboAdmin": true,
      "playdate": "string"
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|arcadeInfo|[ArcadeInfoResponseVO](#schemaarcadeinforesponsevo)|true|none||none|
|thirtyMinutesPlayer|integer(int32)|true|none||三十分钟内玩家|
|oneHourPlayer|integer(int32)|true|none||一小时内玩家|
|twoHoursPlayer|integer(int32)|true|none||两小时内玩家|
|thirtyMinutesPlayCount|integer(int32)|true|none||三十分钟玩家统计|
|oneHourPlayCount|integer(int32)|true|none||一小时玩家统计|
|twoHoursPlayCount|integer(int32)|true|none||两小时玩家统计|
|playerList|[[PlayerList](#schemaplayerlist)]|true|none||玩家列表|
|thirtyMinutesPlayerList|[[PlayerList](#schemaplayerlist)]|true|none||三十分钟玩家列表|

<h2 id="tocS_PlayerList">PlayerList</h2>

<a id="schemaplayerlist"></a>
<a id="schema_PlayerList"></a>
<a id="tocSplayerlist"></a>
<a id="tocsplayerlist"></a>

```json
{
  "userIdHash": "string",
  "maimaiName": "string",
  "turboName": "string",
  "isTurboAdmin": true,
  "playdate": "string"
}

```

三十分钟玩家列表

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|userIdHash|string|true|none||玩家ID哈希|
|maimaiName|string|true|none||maimai名称|
|turboName|string|true|none||turbo名称|
|isTurboAdmin|boolean|true|none||是否为盒子管理|
|playdate|string|true|none||游玩时间|

<h2 id="tocS_AchievementRankingResponseVO">AchievementRankingResponseVO</h2>

<a id="schemaachievementrankingresponsevo"></a>
<a id="schema_AchievementRankingResponseVO"></a>
<a id="tocSachievementrankingresponsevo"></a>
<a id="tocsachievementrankingresponsevo"></a>

```json
{
  "ranking": 0,
  "maimaiName": "string",
  "turboName": "string",
  "achievement": 0.1
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ranking|integer(int32)|true|none||排名|
|maimaiName|string|true|none||maimai名称|
|turboName|string|true|none||turbo名称|
|achievement|number(double)|true|none||达成分数|

<h2 id="tocS_PageDTOAchievementRankingResponseVO">PageDTOAchievementRankingResponseVO</h2>

<a id="schemapagedtoachievementrankingresponsevo"></a>
<a id="schema_PageDTOAchievementRankingResponseVO"></a>
<a id="tocSpagedtoachievementrankingresponsevo"></a>
<a id="tocspagedtoachievementrankingresponsevo"></a>

```json
{
  "content": [
    {
      "ranking": 0,
      "maimaiName": "string",
      "turboName": "string",
      "achievement": 0.1
    }
  ],
  "totalElements": 0,
  "totalPages": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|content|[[AchievementRankingResponseVO](#schemaachievementrankingresponsevo)]|true|none||none|
|totalElements|integer(int64)|true|none||none|
|totalPages|integer(int32)|true|none||none|

