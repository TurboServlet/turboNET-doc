# 游戏数据相关API

## GET 加速盒子-游玩信息

GET /web/turbo

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "show": true,
    "turboInfoList": [
      {
        "name": "string",
        "allRequestsNumber": 0,
        "cacheRequestsNumber": 0,
        "fixedRequestNumber": 0,
        "cacheHitRate": "string",
        "detail": {
          "isEmptyDetail": true,
          "tenMinutesDetail": {},
          "thirtyMinutesDetail": {},
          "hourDetail": {},
          "playerDetail": [
            null
          ]
        }
      }
    ]
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOTurboResponseVO](#schemafinalresponsevoturboresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOTurboResponseVO](#schemafinalresponsevoturboresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOTurboResponseVO](#schemafinalresponsevoturboresponsevo)|

## GET 游戏数据-用户功能票

GET /web/ticket

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "ticketList": [
      {
        "ticketId": 0,
        "ticketName": "string",
        "ticketImg": "string",
        "ticketCount": 0
      }
    ],
    "turboTicketInfo": {
      "ticketId": 0,
      "ticketName": "string",
      "ticketImg": "string"
    },
    "isEnableTurboTicket": true,
    "isTicketEmpty": true
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOTicketResponseVO](#schemafinalresponsevoticketresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOTicketResponseVO](#schemafinalresponsevoticketresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOTicketResponseVO](#schemafinalresponsevoticketresponsevo)|

## POST 游戏设置-锁定用户功能券

POST /web/userOption/upsertTicketWhitelist

> Body 请求参数

```json
{
  "ticketId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[TurboTicketWhitelistRequestVO](#schematurboticketwhitelistrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[Unit](#schemaunit)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[Unit](#schemaunit)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[Unit](#schemaunit)|

## POST 游戏设置-解除用户功能券锁定

POST /web/userOption/deleteTicketWhitelist

需要权限，Admin，Builder，Authorizer

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[Unit](#schemaunit)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[Unit](#schemaunit)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[Unit](#schemaunit)|

## GET 记录-游玩记录

GET /web/record

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "show": true,
    "recordList": [
      {
        "userInfo": {
          "trackNumber": 0,
          "musicPlayDate": "string",
          "isClear": true,
          "isAchievementNewRecord": true,
          "isDxScoreNewRecord": true,
          "comboStatusImg": "string",
          "syncStatusImg": "string",
          "userDxScore": 0,
          "userBeforeRating": 0,
          "userAfterRating": 0,
          "userAchievementStr": "string",
          "userAchievementRankImg": "string",
          "userCombo": 0,
          "maxCombo": 0,
          "userSync": 0,
          "maxSync": 0,
          "dxStarImg": "string"
        },
        "musicInfo": {
          "musicName": "string",
          "musicLevel": 0,
          "musicDiff": "string",
          "musicDiffImg": "string",
          "musicIcon": "string",
          "isDxMusic": true,
          "maxDxScore": 0
        },
        "detailInfo": {
          "isEnabledCriticalPerfect": true,
          "isEnabledFastAndLate": true,
          "fast": 0,
          "late": 0,
          "tap": {},
          "hold": {},
          "slide": {},
          "touch": {},
          "mai2Break": {}
        }
      }
    ]
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVORecordResponseVO](#schemafinalresponsevorecordresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVORecordResponseVO](#schemafinalresponsevorecordresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVORecordResponseVO](#schemafinalresponsevorecordresponsevo)|

## GET 网络状态查询

GET /web/network

包含zlibSkippedCount, retryExceptionCount, panicCount, allPacketNums}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "packets": {
      "zlibSkippedCount": 0,
      "retryExceptionCount": 0,
      "panicCount": 0,
      "allPacketNums": 0
    },
    "packetsBefore": {
      "zlibSkippedCount": 0,
      "retryExceptionCount": 0,
      "panicCount": 0
    }
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVONetworkResponseVO](#schemafinalresponsevonetworkresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVONetworkResponseVO](#schemafinalresponsevonetworkresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVONetworkResponseVO](#schemafinalresponsevonetworkresponsevo)|

## GET 游戏数据-游戏数据

GET /web/playerData

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "achievement": {
      "sssp": 0,
      "sss": 0,
      "ssp": 0,
      "ss": 0,
      "sp": 0,
      "s": 0
    },
    "combo": {
      "app": 0,
      "ap": 0,
      "fcp": 0,
      "fc": 0
    },
    "sync": {
      "fsdp": 0,
      "fsd": 0,
      "fsp": 0,
      "fs": 0
    },
    "userInfo": {
      "name": "string",
      "playCount": 0
    },
    "allMusic": 0
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOPlayerDataResponseVO](#schemafinalresponsevoplayerdataresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOPlayerDataResponseVO](#schemafinalresponsevoplayerdataresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOPlayerDataResponseVO](#schemafinalresponsevoplayerdataresponsevo)|