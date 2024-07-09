# TurboNET Alpha api 文档

Nya~  
marked by 桃玖 & CtrlcvsNya & Kiwi  

Base URLs: https://api.mai-turbo.net  

Swagger3 version (instead of github markdown) : https://api.mai-turbo.net/swagger-ui/index.html

# Authentication

# 网页相关

<a id="opIduserOptionUpsertUserPortraitApi"></a>

## POST 游戏设置-上传用户头像

POST /web/userOption/upsertUserPortrait

> Body 请求参数

```json
{
  "divData": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[UpsertUserPortraitRequestVO](#schemaupsertuserportraitrequestvo)| 否 |none|

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

<a id="opIduserOptionUpsertUserNameApi"></a>

## POST 游戏设置-修改用户名称

POST /web/userOption/upsertUserName

> Body 请求参数

```json
{
  "turboName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[TurboCustomNameRequestVO](#schematurbocustomnamerequestvo)| 否 |none|

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

<a id="opIduserOptionUpsertTicketWhitelistApi"></a>

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

<a id="opIduserOptionDeleteUserPortraitApi"></a>

## POST 游戏设置-删除用户头像

POST /web/userOption/deleteUserPortrait

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

<a id="opIduserOptionDeleteUserNameApi"></a>

## POST 游戏设置-删除用户名称

POST /web/userOption/deleteUserName

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

<a id="opIduserOptionDeleteTicketWhitelistApi"></a>

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

<a id="opIdremoveFavoritePhotoApi"></a>

## POST 相片-移除为用户喜欢相片

POST /web/photo/removeFavoritePhoto

> Body 请求参数

```json
{
  "photoUUID": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[PhotoFavoriteRequestVO](#schemaphotofavoriterequestvo)| 否 |none|

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

<a id="opIdaddFavoritePhotoApi"></a>

## POST 相片-添加为用户喜欢相片

POST /web/photo/addFavoritePhoto

> Body 请求参数

```json
{
  "photoUUID": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[PhotoFavoriteRequestVO](#schemaphotofavoriterequestvo)| 否 |none|

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

<a id="opIdwebUserApi"></a>

## GET 用户（此API不允许BotKey调用）

GET /web/user

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。此界面仅允许正常网页，不允许BotKey调用！|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "username": "string",
    "permissionLevel": "string",
    "email": "string",
    "qqNumber": "string",
    "mai2Name": "string",
    "mai2SHA256": "string",
    "botToken": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOUserResponseVO](#schemafinalresponsevouserresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOUserResponseVO](#schemafinalresponsevouserresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header是否正确|[FinalResponseVOUserResponseVO](#schemafinalresponsevouserresponsevo)|

<a id="opIdturboApi"></a>

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

<a id="opIdticketApi"></a>

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

<a id="opIdrecordApi"></a>

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

<a id="opIduserIgnoredEnableApi"></a>

## GET 排行榜-在排行榜中隐藏自己

GET /web/ranking/userIgnored/enable

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIduserIgnoredDisableApi"></a>

## GET 排行榜-在排行榜中取消隐藏自己

GET /web/ranking/userIgnored/disable

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdtotalAchievementUsersApi"></a>

## GET 排行榜-觉醒排行榜-TurboNET注册用户排行

GET /web/ranking/totalAchievement/users

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerTotalAchievement": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerTotalAchievement": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|

<a id="opIdtotalAchievementApi"></a>

## GET 排行榜-觉醒排行榜-全国加速盒子玩家排行

GET /web/ranking/totalAchievement/everyone

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerTotalAchievement": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerTotalAchievement": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVORankingAchievementResponseVO](#schemafinalresponsevorankingachievementresponsevo)|

<a id="opIddeluxRankingUsersApi"></a>

## GET 排行榜-DX RATING排行榜-TurboNET注册用户排行

GET /web/ranking/deluxRanking/users

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerRating": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerRating": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|

<a id="opIddeluxRankingEveryoneApi"></a>

## GET 排行榜-DX RATING排行榜-全国加速盒子玩家排行

GET /web/ranking/deluxRanking/everyone

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerRating": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerRating": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVORankingResponseVO](#schemafinalresponsevorankingresponsevo)|

<a id="opIdplayerDataApi"></a>

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

<a id="opIdgetHistoryPhotoListApi"></a>

## GET 相片-用户历史相片

GET /web/photo/getHistoryPhotoList

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "photoList": {
      "totalPages": 0,
      "totalElements": 0,
      "size": 0,
      "content": [
        {
          "photoUUID": "string",
          "photoImg": "string",
          "date": "string",
          "isFavorite": true
        }
      ],
      "number": 0,
      "sort": {
        "empty": true,
        "sorted": true,
        "unsorted": true
      },
      "pageable": {
        "offset": 0,
        "sort": {
          "empty": null,
          "sorted": null,
          "unsorted": null
        },
        "paged": true,
        "pageNumber": 0,
        "pageSize": 0,
        "unpaged": true
      },
      "numberOfElements": 0,
      "first": true,
      "last": true,
      "empty": true
    }
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|

<a id="opIdgetFavoritePhotoListApi"></a>

## GET 相片-用户喜爱相片

GET /web/photo/getFavoritePhotoList

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|index|query|Int| 是 |索引|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "photoList": {
      "totalPages": 0,
      "totalElements": 0,
      "size": 0,
      "content": [
        {
          "photoUUID": "string",
          "photoImg": "string",
          "date": "string",
          "isFavorite": true
        }
      ],
      "number": 0,
      "sort": {
        "empty": true,
        "sorted": true,
        "unsorted": true
      },
      "pageable": {
        "offset": 0,
        "sort": {
          "empty": null,
          "sorted": null,
          "unsorted": null
        },
        "paged": true,
        "pageNumber": 0,
        "pageSize": 0,
        "unpaged": true
      },
      "numberOfElements": 0,
      "first": true,
      "last": true,
      "empty": true
    }
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOPhotoResponseVO](#schemafinalresponsevophotoresponsevo)|

<a id="opIdpermissionApi"></a>

## GET 权限展示

GET /web/permission

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
    "permissionLevel": "ADMIN",
    "username": "string",
    "qqNumber": "string",
    "permissionList": [
      {
        "permissionDescription": "string",
        "isGranted": true
      }
    ],
    "authorizationsList": [
      {
        "userBefore": "ADMIN",
        "userAfter": "ADMIN",
        "authorizationUsername": "string",
        "changedDate": "string"
      }
    ],
    "bannedList": [
      {
        "bannedUsername": "string",
        "changedByUsername": "string",
        "changedDate": "string"
      }
    ]
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOPermissionResponseVO](#schemafinalresponsevopermissionresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOPermissionResponseVO](#schemafinalresponsevopermissionresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOPermissionResponseVO](#schemafinalresponsevopermissionresponsevo)|

<a id="opIdnetworkApi"></a>

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

<a id="opIdwebHomeApi"></a>

## GET 用户主页

GET /web/home

包含playerName, playerRating, totalAwake, courseRank, classRank, iconId

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
    "playerName": "string",
    "playerRating": 0,
    "totalAwake": 0,
    "courseRank": 0,
    "classRank": 0,
    "iconId": 0,
    "loginAccount": "string",
    "loginEmail": "string",
    "lastPlayDate": "string",
    "banState": 0,
    "isPortrait": true,
    "portrait": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOHomeResponseVO](#schemafinalresponsevohomeresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOHomeResponseVO](#schemafinalresponsevohomeresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOHomeResponseVO](#schemafinalresponsevohomeresponsevo)|

<a id="opIdcommandQrUdemaeShowAchievementApi"></a>

## GET Turbo盒子工具-机台设置-友人对战完成度显示

GET /web/command/qrUdemaeShowAchievement

需要权限，Admin，Builder

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
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|

<a id="opIdcommandQrPingApi"></a>

## GET Turbo盒子工具-机台设置-PING 机台

GET /web/command/qrPing

需要权限，Admin，Builder

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
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|

<a id="opIdcommandQrMaskUsernameApi"></a>

## GET Turbo盒子工具-机台设置-遮挡用户名

GET /web/command/qrMaskUsername

需要权限，Admin，Builder

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
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|

<a id="opIdcommandQrLoginApi"></a>

## GET Turbo盒子工具-个人设置-Maiturbo NET 加速盒子机台登入

GET /web/command/qrLogin

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
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|

<a id="opIdcommandQrKastanjLoginApi"></a>

## GET Turbo盒子工具-个人设置-Maiturbo NET 加速盒子Kastanj机台登入

GET /web/command/qrKastanjLogin

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
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|请检查权限|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOQrResponseVO](#schemafinalresponsevoqrresponsevo)|

# 授权相关

<a id="opIdunbanUserApi"></a>

## POST 解除用户封禁（此API不允许BotKey调用）

POST /permission/unbanUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。此界面仅允许正常网页，不允许BotKey调用！|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIddeauthorizeUserApi"></a>

## POST 取消授权用户

POST /permission/deauthorizeUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIddeBuilderUserApi"></a>

## POST 取消技术实施员（此API不允许BotKey调用）

POST /permission/deBuilderUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。此界面仅允许正常网页，不允许BotKey调用！|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdbuilderUserApi"></a>

## POST 给予技术实施员（此API不允许BotKey调用）

POST /permission/builderUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。此界面仅允许正常网页，不允许BotKey调用！|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdbanUserApi"></a>

## POST 给予用户封禁（此API不允许BotKey调用）

POST /permission/banUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。此界面仅允许正常网页，不允许BotKey调用！|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdauthorizeUserApi"></a>

## POST 给予授权用户

POST /permission/authorizeUser

> Body 请求参数

```json
{
  "changeUsername": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|
|body|body|[PermissionRequestVO](#schemapermissionrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdshowUserPermissionApi"></a>

## GET 展示用户权限

GET /permission/showUserPermission

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "ADMIN"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOPermissionEnum](#schemafinalresponsevopermissionenum)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOPermissionEnum](#schemafinalresponsevopermissionenum)|

# Bot相关

<a id="opIdunbindApi"></a>

## POST 解绑

POST /bot/unbind

> Body 请求参数

```json
{
  "botKey": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[BotUnbindRequestVO](#schemabotunbindrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOString](#schemafinalresponsevostring)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOString](#schemafinalresponsevostring)|

<a id="opIdbindApi"></a>

## POST 绑定

POST /bot/bind

RequestBody需要两个参数，一个botToken一个botName，botName是由你自己定的，只是用来标记是哪个bot，会在用户前端显示。用户想要绑定，需要去net点击右上角头像，找到botToken。

> Body 请求参数

```json
{
  "botToken": "string",
  "botName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[BotBindRequestVO](#schemabotbindrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "botKey": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOBotBindResponseVO](#schemafinalresponsevobotbindresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOBotBindResponseVO](#schemafinalresponsevobotbindresponsevo)|

<a id="opIdbindListApi"></a>

## GET 绑定列表

GET /bot/bindList

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |权限校验Token。如果为正常网页，那么Bearer开头；如果为Bot，那么BotKey开头。|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": [
    {
      "botKey": "string",
      "botName": "string",
      "useCount": 0,
      "bindDate": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功请求|[FinalResponseVOListBotBindListResponseVO](#schemafinalresponsevolistbotbindlistresponsevo)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|请求失败，请检查header和请求体是否正确|[FinalResponseVOListBotBindListResponseVO](#schemafinalresponsevolistbotbindlistresponsevo)|

# 权限相关

<a id="opIdtokenValidationApi"></a>

## POST token验证

POST /auth/tokenValidation

> Body 请求参数

```json
{
  "token": "string",
  "refreshToken": "string",
  "botToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[TokenValidationRequestVO](#schematokenvalidationrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "token": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVORefreshTokenResponseVO](#schemafinalresponsevorefreshtokenresponsevo)|

<a id="opIduserResetPasswordApi"></a>

## POST 重置密码

POST /auth/resetPassword

> Body 请求参数

```json
{
  "email": "string",
  "captchaToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[ResetPasswordRequestVO](#schemaresetpasswordrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIduserResetPasswordVerifyApi"></a>

## POST 重置密码-验证

POST /auth/resetPassword/verify

> Body 请求参数

```json
{
  "token": "string",
  "valid": "string",
  "password": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[ResetPasswordValidRequestVO](#schemaresetpasswordvalidrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIduserResetPasswordIsValidApi"></a>

## POST 重置密码

POST /auth/resetPassword/isValid

> Body 请求参数

```json
{
  "token": "string",
  "valid": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[ResetPasswordIsValidRequestVO](#schemaresetpasswordisvalidrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIduserRegisterApi"></a>

## POST 注册

POST /auth/register

> Body 请求参数

```json
{
  "username": "string",
  "password": "string",
  "email": "string",
  "qqNumber": "string",
  "weChatID": "string",
  "captchaToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[RegisterRequestVO](#schemaregisterrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "msg": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVORegisterResponseVO](#schemafinalresponsevoregisterresponsevo)|

<a id="opIduserRegisterCommitApi"></a>

## POST 注册验证

POST /auth/register/verify

> Body 请求参数

```json
{
  "token": "string",
  "valid": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[RegisterVerifyRequestVO](#schemaregisterverifyrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIduserRefreshTokenApi"></a>

## POST 刷新Token

POST /auth/refreshToken

> Body 请求参数

```json
{
  "refreshToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[RefreshTokenRequestVO](#schemarefreshtokenrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "token": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVORefreshTokenResponseVO](#schemafinalresponsevorefreshtokenresponsevo)|

<a id="opIduserLogoutApi"></a>

## POST 登出

POST /auth/logout

> Body 请求参数

```json
{
  "token": "string",
  "refreshToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[LogoutRequestVO](#schemalogoutrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIduserLoginApi"></a>

## POST 登录

POST /auth/login

> Body 请求参数

```json
{
  "username": "string",
  "password": "string",
  "captchaToken": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[LoginRequestVO](#schemaloginrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {
    "token": "string",
    "refreshToken": "string"
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVOLoginResponseVO](#schemafinalresponsevologinresponsevo)|

<a id="opIdisUsernameValidApi"></a>

## POST 用户名是否有效

POST /auth/isUsernameValid

> Body 请求参数

```json
{
  "username": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[RegisterUsernameValidRequestVO](#schemaregisterusernamevalidrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

<a id="opIdisSecondStepsValidApi"></a>

## POST 二次确认

POST /auth/isSecondStepsValid

> Body 请求参数

```json
{
  "email": "string",
  "qqNumber": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[RegisterSecondStepsValidRequestVO](#schemaregistersecondstepsvalidrequestvo)| 否 |none|

> 返回示例

> 200 Response

```json
{
  "isSuccess": true,
  "data": {}
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[FinalResponseVONull](#schemafinalresponsevonull)|

# 数据模型

<h2 id="tocS_FinalResponseVOListBotBindListResponseVO">FinalResponseVOListBotBindListResponseVO</h2>

<a id="schemafinalresponsevolistbotbindlistresponsevo"></a>
<a id="schema_FinalResponseVOListBotBindListResponseVO"></a>
<a id="tocSfinalresponsevolistbotbindlistresponsevo"></a>
<a id="tocsfinalresponsevolistbotbindlistresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": [
    {
      "botKey": "string",
      "botName": "string",
      "useCount": 0,
      "bindDate": "string"
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[[BotBindListResponseVO](#schemabotbindlistresponsevo)]|false|none||none|

<h2 id="tocS_BotBindListResponseVO">BotBindListResponseVO</h2>

<a id="schemabotbindlistresponsevo"></a>
<a id="schema_BotBindListResponseVO"></a>
<a id="tocSbotbindlistresponsevo"></a>
<a id="tocsbotbindlistresponsevo"></a>

```json
{
  "botKey": "string",
  "botName": "string",
  "useCount": 0,
  "bindDate": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botKey|string|true|none||none|
|botName|string|true|none||none|
|useCount|integer(int32)|true|none||none|
|bindDate|string|true|none||none|

<h2 id="tocS_FinalResponseVOPermissionEnum">FinalResponseVOPermissionEnum</h2>

<a id="schemafinalresponsevopermissionenum"></a>
<a id="schema_FinalResponseVOPermissionEnum"></a>
<a id="tocSfinalresponsevopermissionenum"></a>
<a id="tocsfinalresponsevopermissionenum"></a>

```json
{
  "isSuccess": true,
  "data": "ADMIN"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|data|ADMIN|
|data|BUILDER|
|data|AUTHORIZER|
|data|USER|
|data|BANNED|

<h2 id="tocS_QrResponseVO">QrResponseVO</h2>

<a id="schemaqrresponsevo"></a>
<a id="schema_QrResponseVO"></a>
<a id="tocSqrresponsevo"></a>
<a id="tocsqrresponsevo"></a>

```json
{
  "qrCodeBase64": "string",
  "qrCodeValidTime": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|qrCodeBase64|string|true|none||none|
|qrCodeValidTime|string|true|none||none|

<h2 id="tocS_FinalResponseVOQrResponseVO">FinalResponseVOQrResponseVO</h2>

<a id="schemafinalresponsevoqrresponsevo"></a>
<a id="schema_FinalResponseVOQrResponseVO"></a>
<a id="tocSfinalresponsevoqrresponsevo"></a>
<a id="tocsfinalresponsevoqrresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "qrCodeBase64": "string",
    "qrCodeValidTime": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[QrResponseVO](#schemaqrresponsevo)|false|none||none|

<h2 id="tocS_HomeResponseVO">HomeResponseVO</h2>

<a id="schemahomeresponsevo"></a>
<a id="schema_HomeResponseVO"></a>
<a id="tocShomeresponsevo"></a>
<a id="tocshomeresponsevo"></a>

```json
{
  "playerName": "string",
  "playerRating": 0,
  "totalAwake": 0,
  "courseRank": 0,
  "classRank": 0,
  "iconId": 0,
  "loginAccount": "string",
  "loginEmail": "string",
  "lastPlayDate": "string",
  "banState": 0,
  "isPortrait": true,
  "portrait": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerName|string|true|none||none|
|playerRating|integer(int32)|true|none||none|
|totalAwake|integer(int32)|true|none||none|
|courseRank|integer(int32)|true|none||none|
|classRank|integer(int32)|true|none||none|
|iconId|integer(int32)|true|none||none|
|loginAccount|string|true|none||none|
|loginEmail|string|true|none||none|
|lastPlayDate|string|true|none||none|
|banState|integer(int32)|true|none||none|
|isPortrait|boolean|true|none||none|
|portrait|string|false|none||none|

<h2 id="tocS_FinalResponseVOHomeResponseVO">FinalResponseVOHomeResponseVO</h2>

<a id="schemafinalresponsevohomeresponsevo"></a>
<a id="schema_FinalResponseVOHomeResponseVO"></a>
<a id="tocSfinalresponsevohomeresponsevo"></a>
<a id="tocsfinalresponsevohomeresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "playerName": "string",
    "playerRating": 0,
    "totalAwake": 0,
    "courseRank": 0,
    "classRank": 0,
    "iconId": 0,
    "loginAccount": "string",
    "loginEmail": "string",
    "lastPlayDate": "string",
    "banState": 0,
    "isPortrait": true,
    "portrait": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[HomeResponseVO](#schemahomeresponsevo)|false|none||none|

<h2 id="tocS_PacketResultHourDTO">PacketResultHourDTO</h2>

<a id="schemapacketresulthourdto"></a>
<a id="schema_PacketResultHourDTO"></a>
<a id="tocSpacketresulthourdto"></a>
<a id="tocspacketresulthourdto"></a>

```json
{
  "zlibSkippedCount": 0,
  "retryExceptionCount": 0,
  "panicCount": 0,
  "allPacketNums": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|zlibSkippedCount|integer(int32)|true|none||none|
|retryExceptionCount|integer(int32)|true|none||none|
|panicCount|integer(int32)|true|none||none|
|allPacketNums|integer(int32)|true|none||none|

<h2 id="tocS_PacketResultBeforeDTO">PacketResultBeforeDTO</h2>

<a id="schemapacketresultbeforedto"></a>
<a id="schema_PacketResultBeforeDTO"></a>
<a id="tocSpacketresultbeforedto"></a>
<a id="tocspacketresultbeforedto"></a>

```json
{
  "zlibSkippedCount": 0,
  "retryExceptionCount": 0,
  "panicCount": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|zlibSkippedCount|integer(int32)|true|none||none|
|retryExceptionCount|integer(int32)|true|none||none|
|panicCount|integer(int32)|true|none||none|

<h2 id="tocS_NetworkResponseVO">NetworkResponseVO</h2>

<a id="schemanetworkresponsevo"></a>
<a id="schema_NetworkResponseVO"></a>
<a id="tocSnetworkresponsevo"></a>
<a id="tocsnetworkresponsevo"></a>

```json
{
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

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|packets|[PacketResultHourDTO](#schemapacketresulthourdto)|true|none||none|
|packetsBefore|[PacketResultBeforeDTO](#schemapacketresultbeforedto)|true|none||none|

<h2 id="tocS_FinalResponseVONetworkResponseVO">FinalResponseVONetworkResponseVO</h2>

<a id="schemafinalresponsevonetworkresponsevo"></a>
<a id="schema_FinalResponseVONetworkResponseVO"></a>
<a id="tocSfinalresponsevonetworkresponsevo"></a>
<a id="tocsfinalresponsevonetworkresponsevo"></a>

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

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[NetworkResponseVO](#schemanetworkresponsevo)|false|none||none|

<h2 id="tocS_PermissionResponseVO">PermissionResponseVO</h2>

<a id="schemapermissionresponsevo"></a>
<a id="schema_PermissionResponseVO"></a>
<a id="tocSpermissionresponsevo"></a>
<a id="tocspermissionresponsevo"></a>

```json
{
  "permissionLevel": "ADMIN",
  "username": "string",
  "qqNumber": "string",
  "permissionList": [
    {
      "permissionDescription": "string",
      "isGranted": true
    }
  ],
  "authorizationsList": [
    {
      "userBefore": "ADMIN",
      "userAfter": "ADMIN",
      "authorizationUsername": "string",
      "changedDate": "string"
    }
  ],
  "bannedList": [
    {
      "bannedUsername": "string",
      "changedByUsername": "string",
      "changedDate": "string"
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|permissionLevel|string|true|none||none|
|username|string|true|none||none|
|qqNumber|string|true|none||none|
|permissionList|[[PermissionListResponseVO](#schemapermissionlistresponsevo)]|true|none||none|
|authorizationsList|[[AuthorizationResponseVO](#schemaauthorizationresponsevo)]|true|none||none|
|bannedList|[[BanResponseVO](#schemabanresponsevo)]|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|permissionLevel|ADMIN|
|permissionLevel|BUILDER|
|permissionLevel|AUTHORIZER|
|permissionLevel|USER|
|permissionLevel|BANNED|

<h2 id="tocS_PermissionListResponseVO">PermissionListResponseVO</h2>

<a id="schemapermissionlistresponsevo"></a>
<a id="schema_PermissionListResponseVO"></a>
<a id="tocSpermissionlistresponsevo"></a>
<a id="tocspermissionlistresponsevo"></a>

```json
{
  "permissionDescription": "string",
  "isGranted": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|permissionDescription|string|true|none||none|
|isGranted|boolean|true|none||none|

<h2 id="tocS_FinalResponseVOPermissionResponseVO">FinalResponseVOPermissionResponseVO</h2>

<a id="schemafinalresponsevopermissionresponsevo"></a>
<a id="schema_FinalResponseVOPermissionResponseVO"></a>
<a id="tocSfinalresponsevopermissionresponsevo"></a>
<a id="tocsfinalresponsevopermissionresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "permissionLevel": "ADMIN",
    "username": "string",
    "qqNumber": "string",
    "permissionList": [
      {
        "permissionDescription": "string",
        "isGranted": true
      }
    ],
    "authorizationsList": [
      {
        "userBefore": "ADMIN",
        "userAfter": "ADMIN",
        "authorizationUsername": "string",
        "changedDate": "string"
      }
    ],
    "bannedList": [
      {
        "bannedUsername": "string",
        "changedByUsername": "string",
        "changedDate": "string"
      }
    ]
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[PermissionResponseVO](#schemapermissionresponsevo)|false|none||none|

<h2 id="tocS_BanResponseVO">BanResponseVO</h2>

<a id="schemabanresponsevo"></a>
<a id="schema_BanResponseVO"></a>
<a id="tocSbanresponsevo"></a>
<a id="tocsbanresponsevo"></a>

```json
{
  "bannedUsername": "string",
  "changedByUsername": "string",
  "changedDate": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bannedUsername|string|true|none||none|
|changedByUsername|string|true|none||none|
|changedDate|string|true|none||none|

<h2 id="tocS_AuthorizationResponseVO">AuthorizationResponseVO</h2>

<a id="schemaauthorizationresponsevo"></a>
<a id="schema_AuthorizationResponseVO"></a>
<a id="tocSauthorizationresponsevo"></a>
<a id="tocsauthorizationresponsevo"></a>

```json
{
  "userBefore": "ADMIN",
  "userAfter": "ADMIN",
  "authorizationUsername": "string",
  "changedDate": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|userBefore|string|true|none||none|
|userAfter|string|true|none||none|
|authorizationUsername|string|true|none||none|
|changedDate|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|userBefore|ADMIN|
|userBefore|BUILDER|
|userBefore|AUTHORIZER|
|userBefore|USER|
|userBefore|BANNED|
|userAfter|ADMIN|
|userAfter|BUILDER|
|userAfter|AUTHORIZER|
|userAfter|USER|
|userAfter|BANNED|

<h2 id="tocS_SortObject">SortObject</h2>

<a id="schemasortobject"></a>
<a id="schema_SortObject"></a>
<a id="tocSsortobject"></a>
<a id="tocssortobject"></a>

```json
{
  "empty": true,
  "sorted": true,
  "unsorted": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|empty|boolean|false|none||none|
|sorted|boolean|false|none||none|
|unsorted|boolean|false|none||none|

<h2 id="tocS_PhotoResponseVO">PhotoResponseVO</h2>

<a id="schemaphotoresponsevo"></a>
<a id="schema_PhotoResponseVO"></a>
<a id="tocSphotoresponsevo"></a>
<a id="tocsphotoresponsevo"></a>

```json
{
  "photoList": {
    "totalPages": 0,
    "totalElements": 0,
    "size": 0,
    "content": [
      {
        "photoUUID": "string",
        "photoImg": "string",
        "date": "string",
        "isFavorite": true
      }
    ],
    "number": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageable": {
      "offset": 0,
      "sort": {
        "empty": true,
        "sorted": true,
        "unsorted": true
      },
      "paged": true,
      "pageNumber": 0,
      "pageSize": 0,
      "unpaged": true
    },
    "numberOfElements": 0,
    "first": true,
    "last": true,
    "empty": true
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoList|[PagePhotoListVO](#schemapagephotolistvo)|true|none||none|

<h2 id="tocS_PhotoListVO">PhotoListVO</h2>

<a id="schemaphotolistvo"></a>
<a id="schema_PhotoListVO"></a>
<a id="tocSphotolistvo"></a>
<a id="tocsphotolistvo"></a>

```json
{
  "photoUUID": "string",
  "photoImg": "string",
  "date": "string",
  "isFavorite": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoUUID|string|true|none||none|
|photoImg|string(byte)|true|none||none|
|date|string|true|none||none|
|isFavorite|boolean|true|none||none|

<h2 id="tocS_PageableObject">PageableObject</h2>

<a id="schemapageableobject"></a>
<a id="schema_PageableObject"></a>
<a id="tocSpageableobject"></a>
<a id="tocspageableobject"></a>

```json
{
  "offset": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "paged": true,
  "pageNumber": 0,
  "pageSize": 0,
  "unpaged": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|offset|integer(int64)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|paged|boolean|false|none||none|
|pageNumber|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|unpaged|boolean|false|none||none|

<h2 id="tocS_PagePhotoListVO">PagePhotoListVO</h2>

<a id="schemapagephotolistvo"></a>
<a id="schema_PagePhotoListVO"></a>
<a id="tocSpagephotolistvo"></a>
<a id="tocspagephotolistvo"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "photoUUID": "string",
      "photoImg": "string",
      "date": "string",
      "isFavorite": true
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "paged": true,
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true
  },
  "numberOfElements": 0,
  "first": true,
  "last": true,
  "empty": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[PhotoListVO](#schemaphotolistvo)]|false|none||none|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|first|boolean|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_FinalResponseVOPhotoResponseVO">FinalResponseVOPhotoResponseVO</h2>

<a id="schemafinalresponsevophotoresponsevo"></a>
<a id="schema_FinalResponseVOPhotoResponseVO"></a>
<a id="tocSfinalresponsevophotoresponsevo"></a>
<a id="tocsfinalresponsevophotoresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "photoList": {
      "totalPages": 0,
      "totalElements": 0,
      "size": 0,
      "content": [
        {
          "photoUUID": "string",
          "photoImg": "string",
          "date": "string",
          "isFavorite": true
        }
      ],
      "number": 0,
      "sort": {
        "empty": true,
        "sorted": true,
        "unsorted": true
      },
      "pageable": {
        "offset": 0,
        "sort": {
          "empty": null,
          "sorted": null,
          "unsorted": null
        },
        "paged": true,
        "pageNumber": 0,
        "pageSize": 0,
        "unpaged": true
      },
      "numberOfElements": 0,
      "first": true,
      "last": true,
      "empty": true
    }
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[PhotoResponseVO](#schemaphotoresponsevo)|false|none||none|

<h2 id="tocS_UserInfoVO">UserInfoVO</h2>

<a id="schemauserinfovo"></a>
<a id="schema_UserInfoVO"></a>
<a id="tocSuserinfovo"></a>
<a id="tocsuserinfovo"></a>

```json
{
  "name": "string",
  "playCount": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|name|string|true|none||none|
|playCount|integer(int32)|true|none||none|

<h2 id="tocS_SyncVO">SyncVO</h2>

<a id="schemasyncvo"></a>
<a id="schema_SyncVO"></a>
<a id="tocSsyncvo"></a>
<a id="tocssyncvo"></a>

```json
{
  "fsdp": 0,
  "fsd": 0,
  "fsp": 0,
  "fs": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|fsdp|integer(int32)|true|none||none|
|fsd|integer(int32)|true|none||none|
|fsp|integer(int32)|true|none||none|
|fs|integer(int32)|true|none||none|

<h2 id="tocS_PlayerDataResponseVO">PlayerDataResponseVO</h2>

<a id="schemaplayerdataresponsevo"></a>
<a id="schema_PlayerDataResponseVO"></a>
<a id="tocSplayerdataresponsevo"></a>
<a id="tocsplayerdataresponsevo"></a>

```json
{
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

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|achievement|[AchievementVO](#schemaachievementvo)|true|none||none|
|combo|[ComboVO](#schemacombovo)|true|none||none|
|sync|[SyncVO](#schemasyncvo)|true|none||none|
|userInfo|[UserInfoVO](#schemauserinfovo)|true|none||none|
|allMusic|integer(int32)|true|none||none|

<h2 id="tocS_FinalResponseVOPlayerDataResponseVO">FinalResponseVOPlayerDataResponseVO</h2>

<a id="schemafinalresponsevoplayerdataresponsevo"></a>
<a id="schema_FinalResponseVOPlayerDataResponseVO"></a>
<a id="tocSfinalresponsevoplayerdataresponsevo"></a>
<a id="tocsfinalresponsevoplayerdataresponsevo"></a>

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

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[PlayerDataResponseVO](#schemaplayerdataresponsevo)|false|none||none|

<h2 id="tocS_ComboVO">ComboVO</h2>

<a id="schemacombovo"></a>
<a id="schema_ComboVO"></a>
<a id="tocScombovo"></a>
<a id="tocscombovo"></a>

```json
{
  "app": 0,
  "ap": 0,
  "fcp": 0,
  "fc": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|app|integer(int32)|true|none||none|
|ap|integer(int32)|true|none||none|
|fcp|integer(int32)|true|none||none|
|fc|integer(int32)|true|none||none|

<h2 id="tocS_AchievementVO">AchievementVO</h2>

<a id="schemaachievementvo"></a>
<a id="schema_AchievementVO"></a>
<a id="tocSachievementvo"></a>
<a id="tocsachievementvo"></a>

```json
{
  "sssp": 0,
  "sss": 0,
  "ssp": 0,
  "ss": 0,
  "sp": 0,
  "s": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|sssp|integer(int32)|true|none||none|
|sss|integer(int32)|true|none||none|
|ssp|integer(int32)|true|none||none|
|ss|integer(int32)|true|none||none|
|sp|integer(int32)|true|none||none|
|s|integer(int32)|true|none||none|

<h2 id="tocS_UserRanking">UserRanking</h2>

<a id="schemauserranking"></a>
<a id="schema_UserRanking"></a>
<a id="tocSuserranking"></a>
<a id="tocsuserranking"></a>

```json
{
  "playerRanking": 0,
  "playerRating": 0,
  "playerPercent": 0,
  "isIgnored": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerRanking|integer(int32)|true|none||none|
|playerRating|integer(int32)|true|none||none|
|playerPercent|number(double)|true|none||none|
|isIgnored|boolean|true|none||none|

<h2 id="tocS_SinglePlayerRanking">SinglePlayerRanking</h2>

<a id="schemasingleplayerranking"></a>
<a id="schema_SinglePlayerRanking"></a>
<a id="tocSsingleplayerranking"></a>
<a id="tocssingleplayerranking"></a>

```json
{
  "playerRanking": 0,
  "playerName": "string",
  "playerRating": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerRanking|integer(int32)|true|none||none|
|playerName|string|true|none||none|
|playerRating|integer(int32)|true|none||none|

<h2 id="tocS_RankingResponseVO">RankingResponseVO</h2>

<a id="schemarankingresponsevo"></a>
<a id="schema_RankingResponseVO"></a>
<a id="tocSrankingresponsevo"></a>
<a id="tocsrankingresponsevo"></a>

```json
{
  "singlePlayerRanking": [
    {
      "playerRanking": 0,
      "playerName": "string",
      "playerRating": 0
    }
  ],
  "userRanking": {
    "playerRanking": 0,
    "playerRating": 0,
    "playerPercent": 0,
    "isIgnored": true
  },
  "totalPages": 0,
  "totalElements": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|singlePlayerRanking|[[SinglePlayerRanking](#schemasingleplayerranking)]|true|none||none|
|userRanking|[UserRanking](#schemauserranking)|true|none||none|
|totalPages|integer(int32)|true|none||none|
|totalElements|integer(int64)|true|none||none|

<h2 id="tocS_FinalResponseVORankingResponseVO">FinalResponseVORankingResponseVO</h2>

<a id="schemafinalresponsevorankingresponsevo"></a>
<a id="schema_FinalResponseVORankingResponseVO"></a>
<a id="tocSfinalresponsevorankingresponsevo"></a>
<a id="tocsfinalresponsevorankingresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerRating": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerRating": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[RankingResponseVO](#schemarankingresponsevo)|false|none||none|

<h2 id="tocS_UserAchievementRanking">UserAchievementRanking</h2>

<a id="schemauserachievementranking"></a>
<a id="schema_UserAchievementRanking"></a>
<a id="tocSuserachievementranking"></a>
<a id="tocsuserachievementranking"></a>

```json
{
  "playerRanking": 0,
  "playerTotalAchievement": 0,
  "playerPercent": 0,
  "isIgnored": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerRanking|integer(int32)|true|none||none|
|playerTotalAchievement|integer(int64)|true|none||none|
|playerPercent|number(double)|true|none||none|
|isIgnored|boolean|true|none||none|

<h2 id="tocS_SinglePlayerAchievementRanking">SinglePlayerAchievementRanking</h2>

<a id="schemasingleplayerachievementranking"></a>
<a id="schema_SinglePlayerAchievementRanking"></a>
<a id="tocSsingleplayerachievementranking"></a>
<a id="tocssingleplayerachievementranking"></a>

```json
{
  "playerRanking": 0,
  "playerName": "string",
  "playerTotalAchievement": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerRanking|integer(int32)|true|none||none|
|playerName|string|true|none||none|
|playerTotalAchievement|integer(int64)|true|none||none|

<h2 id="tocS_RankingAchievementResponseVO">RankingAchievementResponseVO</h2>

<a id="schemarankingachievementresponsevo"></a>
<a id="schema_RankingAchievementResponseVO"></a>
<a id="tocSrankingachievementresponsevo"></a>
<a id="tocsrankingachievementresponsevo"></a>

```json
{
  "singlePlayerRanking": [
    {
      "playerRanking": 0,
      "playerName": "string",
      "playerTotalAchievement": 0
    }
  ],
  "userRanking": {
    "playerRanking": 0,
    "playerTotalAchievement": 0,
    "playerPercent": 0,
    "isIgnored": true
  },
  "totalPages": 0,
  "totalElements": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|singlePlayerRanking|[[SinglePlayerAchievementRanking](#schemasingleplayerachievementranking)]|true|none||none|
|userRanking|[UserAchievementRanking](#schemauserachievementranking)|true|none||none|
|totalPages|integer(int32)|true|none||none|
|totalElements|integer(int64)|true|none||none|

<h2 id="tocS_FinalResponseVORankingAchievementResponseVO">FinalResponseVORankingAchievementResponseVO</h2>

<a id="schemafinalresponsevorankingachievementresponsevo"></a>
<a id="schema_FinalResponseVORankingAchievementResponseVO"></a>
<a id="tocSfinalresponsevorankingachievementresponsevo"></a>
<a id="tocsfinalresponsevorankingachievementresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "singlePlayerRanking": [
      {
        "playerRanking": 0,
        "playerName": "string",
        "playerTotalAchievement": 0
      }
    ],
    "userRanking": {
      "playerRanking": 0,
      "playerTotalAchievement": 0,
      "playerPercent": 0,
      "isIgnored": true
    },
    "totalPages": 0,
    "totalElements": 0
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[RankingAchievementResponseVO](#schemarankingachievementresponsevo)|false|none||none|

<h2 id="tocS_UserInfo">UserInfo</h2>

<a id="schemauserinfo"></a>
<a id="schema_UserInfo"></a>
<a id="tocSuserinfo"></a>
<a id="tocsuserinfo"></a>

```json
{
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
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|trackNumber|integer(int32)|true|none||none|
|musicPlayDate|string|true|none||none|
|isClear|boolean|true|none||none|
|isAchievementNewRecord|boolean|true|none||none|
|isDxScoreNewRecord|boolean|true|none||none|
|comboStatusImg|string|true|none||none|
|syncStatusImg|string|true|none||none|
|userDxScore|integer(int32)|true|none||none|
|userBeforeRating|integer(int32)|true|none||none|
|userAfterRating|integer(int32)|true|none||none|
|userAchievementStr|string|true|none||none|
|userAchievementRankImg|string|true|none||none|
|userCombo|integer(int32)|true|none||none|
|maxCombo|integer(int32)|true|none||none|
|userSync|integer(int32)|true|none||none|
|maxSync|integer(int32)|true|none||none|
|dxStarImg|string|true|none||none|

<h2 id="tocS_RecordResponseVO">RecordResponseVO</h2>

<a id="schemarecordresponsevo"></a>
<a id="schema_RecordResponseVO"></a>
<a id="tocSrecordresponsevo"></a>
<a id="tocsrecordresponsevo"></a>

```json
{
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
        "tap": {
          "criticalPerfect": 0,
          "perfect": 0,
          "great": 0,
          "good": 0,
          "miss": 0
        },
        "hold": {
          "criticalPerfect": 0,
          "perfect": 0,
          "great": 0,
          "good": 0,
          "miss": 0
        },
        "slide": {
          "criticalPerfect": 0,
          "perfect": 0,
          "great": 0,
          "good": 0,
          "miss": 0
        },
        "touch": {
          "criticalPerfect": 0,
          "perfect": 0,
          "great": 0,
          "good": 0,
          "miss": 0
        },
        "mai2Break": {
          "criticalPerfect": 0,
          "perfect": 0,
          "great": 0,
          "good": 0,
          "miss": 0
        }
      }
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|show|boolean|true|none||none|
|recordList|[[Mai2Record](#schemamai2record)]|true|none||none|

<h2 id="tocS_NotesInfo">NotesInfo</h2>

<a id="schemanotesinfo"></a>
<a id="schema_NotesInfo"></a>
<a id="tocSnotesinfo"></a>
<a id="tocsnotesinfo"></a>

```json
{
  "criticalPerfect": 0,
  "perfect": 0,
  "great": 0,
  "good": 0,
  "miss": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|criticalPerfect|integer(int32)|true|none||none|
|perfect|integer(int32)|true|none||none|
|great|integer(int32)|true|none||none|
|good|integer(int32)|true|none||none|
|miss|integer(int32)|true|none||none|

<h2 id="tocS_MusicInfo">MusicInfo</h2>

<a id="schemamusicinfo"></a>
<a id="schema_MusicInfo"></a>
<a id="tocSmusicinfo"></a>
<a id="tocsmusicinfo"></a>

```json
{
  "musicName": "string",
  "musicLevel": 0,
  "musicDiff": "string",
  "musicDiffImg": "string",
  "musicIcon": "string",
  "isDxMusic": true,
  "maxDxScore": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|musicName|string|true|none||none|
|musicLevel|integer(int32)|true|none||none|
|musicDiff|string|true|none||none|
|musicDiffImg|string|true|none||none|
|musicIcon|string|true|none||none|
|isDxMusic|boolean|true|none||none|
|maxDxScore|integer(int32)|true|none||none|

<h2 id="tocS_Mai2Record">Mai2Record</h2>

<a id="schemamai2record"></a>
<a id="schema_Mai2Record"></a>
<a id="tocSmai2record"></a>
<a id="tocsmai2record"></a>

```json
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
    "tap": {
      "criticalPerfect": 0,
      "perfect": 0,
      "great": 0,
      "good": 0,
      "miss": 0
    },
    "hold": {
      "criticalPerfect": 0,
      "perfect": 0,
      "great": 0,
      "good": 0,
      "miss": 0
    },
    "slide": {
      "criticalPerfect": 0,
      "perfect": 0,
      "great": 0,
      "good": 0,
      "miss": 0
    },
    "touch": {
      "criticalPerfect": 0,
      "perfect": 0,
      "great": 0,
      "good": 0,
      "miss": 0
    },
    "mai2Break": {
      "criticalPerfect": 0,
      "perfect": 0,
      "great": 0,
      "good": 0,
      "miss": 0
    }
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|userInfo|[UserInfo](#schemauserinfo)|true|none||none|
|musicInfo|[MusicInfo](#schemamusicinfo)|true|none||none|
|detailInfo|[DetailInfo](#schemadetailinfo)|true|none||none|

<h2 id="tocS_FinalResponseVORecordResponseVO">FinalResponseVORecordResponseVO</h2>

<a id="schemafinalresponsevorecordresponsevo"></a>
<a id="schema_FinalResponseVORecordResponseVO"></a>
<a id="tocSfinalresponsevorecordresponsevo"></a>
<a id="tocsfinalresponsevorecordresponsevo"></a>

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

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[RecordResponseVO](#schemarecordresponsevo)|false|none||none|

<h2 id="tocS_DetailInfo">DetailInfo</h2>

<a id="schemadetailinfo"></a>
<a id="schema_DetailInfo"></a>
<a id="tocSdetailinfo"></a>
<a id="tocsdetailinfo"></a>

```json
{
  "isEnabledCriticalPerfect": true,
  "isEnabledFastAndLate": true,
  "fast": 0,
  "late": 0,
  "tap": {
    "criticalPerfect": 0,
    "perfect": 0,
    "great": 0,
    "good": 0,
    "miss": 0
  },
  "hold": {
    "criticalPerfect": 0,
    "perfect": 0,
    "great": 0,
    "good": 0,
    "miss": 0
  },
  "slide": {
    "criticalPerfect": 0,
    "perfect": 0,
    "great": 0,
    "good": 0,
    "miss": 0
  },
  "touch": {
    "criticalPerfect": 0,
    "perfect": 0,
    "great": 0,
    "good": 0,
    "miss": 0
  },
  "mai2Break": {
    "criticalPerfect": 0,
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
|isEnabledCriticalPerfect|boolean|true|none||none|
|isEnabledFastAndLate|boolean|true|none||none|
|fast|integer(int32)|true|none||none|
|late|integer(int32)|true|none||none|
|tap|[NotesInfo](#schemanotesinfo)|true|none||none|
|hold|[NotesInfo](#schemanotesinfo)|true|none||none|
|slide|[NotesInfo](#schemanotesinfo)|true|none||none|
|touch|[NotesInfo](#schemanotesinfo)|true|none||none|
|mai2Break|[NotesInfo](#schemanotesinfo)|true|none||none|

<h2 id="tocS_TurboTicketInfoVO">TurboTicketInfoVO</h2>

<a id="schematurboticketinfovo"></a>
<a id="schema_TurboTicketInfoVO"></a>
<a id="tocSturboticketinfovo"></a>
<a id="tocsturboticketinfovo"></a>

```json
{
  "ticketId": 0,
  "ticketName": "string",
  "ticketImg": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||none|
|ticketName|string|true|none||none|
|ticketImg|string|true|none||none|

<h2 id="tocS_TicketVO">TicketVO</h2>

<a id="schematicketvo"></a>
<a id="schema_TicketVO"></a>
<a id="tocSticketvo"></a>
<a id="tocsticketvo"></a>

```json
{
  "ticketId": 0,
  "ticketName": "string",
  "ticketImg": "string",
  "ticketCount": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||none|
|ticketName|string|true|none||none|
|ticketImg|string|true|none||none|
|ticketCount|integer(int32)|true|none||none|

<h2 id="tocS_TicketResponseVO">TicketResponseVO</h2>

<a id="schematicketresponsevo"></a>
<a id="schema_TicketResponseVO"></a>
<a id="tocSticketresponsevo"></a>
<a id="tocsticketresponsevo"></a>

```json
{
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

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketList|[[TicketVO](#schematicketvo)]|true|none||none|
|turboTicketInfo|[TurboTicketInfoVO](#schematurboticketinfovo)|false|none||none|
|isEnableTurboTicket|boolean|true|none||none|
|isTicketEmpty|boolean|true|none||none|

<h2 id="tocS_FinalResponseVOTicketResponseVO">FinalResponseVOTicketResponseVO</h2>

<a id="schemafinalresponsevoticketresponsevo"></a>
<a id="schema_FinalResponseVOTicketResponseVO"></a>
<a id="tocSfinalresponsevoticketresponsevo"></a>
<a id="tocsfinalresponsevoticketresponsevo"></a>

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

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[TicketResponseVO](#schematicketresponsevo)|false|none||none|

<h2 id="tocS_TurboVO">TurboVO</h2>

<a id="schematurbovo"></a>
<a id="schema_TurboVO"></a>
<a id="tocSturbovo"></a>
<a id="tocsturbovo"></a>

```json
{
  "name": "string",
  "allRequestsNumber": 0,
  "cacheRequestsNumber": 0,
  "fixedRequestNumber": 0,
  "cacheHitRate": "string",
  "detail": {
    "isEmptyDetail": true,
    "tenMinutesDetail": {
      "playerCount": 0,
      "playCount": 0
    },
    "thirtyMinutesDetail": {
      "playerCount": 0,
      "playCount": 0
    },
    "hourDetail": {
      "playerCount": 0,
      "playCount": 0
    },
    "playerDetail": [
      {
        "playerLoginDate": "string",
        "playerName": "string",
        "playerRating": 0
      }
    ]
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|name|string|true|none||none|
|allRequestsNumber|integer(int32)|true|none||none|
|cacheRequestsNumber|integer(int32)|true|none||none|
|fixedRequestNumber|integer(int32)|true|none||none|
|cacheHitRate|string|true|none||none|
|detail|[TurboDetailResponseVO](#schematurbodetailresponsevo)|true|none||none|

<h2 id="tocS_TurboSingleDetailPlayerVO">TurboSingleDetailPlayerVO</h2>

<a id="schematurbosingledetailplayervo"></a>
<a id="schema_TurboSingleDetailPlayerVO"></a>
<a id="tocSturbosingledetailplayervo"></a>
<a id="tocsturbosingledetailplayervo"></a>

```json
{
  "playerLoginDate": "string",
  "playerName": "string",
  "playerRating": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerLoginDate|string|true|none||none|
|playerName|string|true|none||none|
|playerRating|integer(int32)|true|none||none|

<h2 id="tocS_TurboResponseVO">TurboResponseVO</h2>

<a id="schematurboresponsevo"></a>
<a id="schema_TurboResponseVO"></a>
<a id="tocSturboresponsevo"></a>
<a id="tocsturboresponsevo"></a>

```json
{
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
        "tenMinutesDetail": {
          "playerCount": 0,
          "playCount": 0
        },
        "thirtyMinutesDetail": {
          "playerCount": 0,
          "playCount": 0
        },
        "hourDetail": {
          "playerCount": 0,
          "playCount": 0
        },
        "playerDetail": [
          {
            "playerLoginDate": null,
            "playerName": null,
            "playerRating": null
          }
        ]
      }
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|show|boolean|true|none||none|
|turboInfoList|[[TurboVO](#schematurbovo)]|true|none||none|

<h2 id="tocS_TurboPlayDetailVO">TurboPlayDetailVO</h2>

<a id="schematurboplaydetailvo"></a>
<a id="schema_TurboPlayDetailVO"></a>
<a id="tocSturboplaydetailvo"></a>
<a id="tocsturboplaydetailvo"></a>

```json
{
  "playerCount": 0,
  "playCount": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|playerCount|integer(int32)|true|none||none|
|playCount|integer(int32)|true|none||none|

<h2 id="tocS_TurboDetailResponseVO">TurboDetailResponseVO</h2>

<a id="schematurbodetailresponsevo"></a>
<a id="schema_TurboDetailResponseVO"></a>
<a id="tocSturbodetailresponsevo"></a>
<a id="tocsturbodetailresponsevo"></a>

```json
{
  "isEmptyDetail": true,
  "tenMinutesDetail": {
    "playerCount": 0,
    "playCount": 0
  },
  "thirtyMinutesDetail": {
    "playerCount": 0,
    "playCount": 0
  },
  "hourDetail": {
    "playerCount": 0,
    "playCount": 0
  },
  "playerDetail": [
    {
      "playerLoginDate": "string",
      "playerName": "string",
      "playerRating": 0
    }
  ]
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isEmptyDetail|boolean|true|none||none|
|tenMinutesDetail|[TurboPlayDetailVO](#schematurboplaydetailvo)|true|none||none|
|thirtyMinutesDetail|[TurboPlayDetailVO](#schematurboplaydetailvo)|true|none||none|
|hourDetail|[TurboPlayDetailVO](#schematurboplaydetailvo)|true|none||none|
|playerDetail|[[TurboSingleDetailPlayerVO](#schematurbosingledetailplayervo)]|true|none||none|

<h2 id="tocS_FinalResponseVOTurboResponseVO">FinalResponseVOTurboResponseVO</h2>

<a id="schemafinalresponsevoturboresponsevo"></a>
<a id="schema_FinalResponseVOTurboResponseVO"></a>
<a id="tocSfinalresponsevoturboresponsevo"></a>
<a id="tocsfinalresponsevoturboresponsevo"></a>

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

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[TurboResponseVO](#schematurboresponsevo)|false|none||none|

<h2 id="tocS_UserResponseVO">UserResponseVO</h2>

<a id="schemauserresponsevo"></a>
<a id="schema_UserResponseVO"></a>
<a id="tocSuserresponsevo"></a>
<a id="tocsuserresponsevo"></a>

```json
{
  "username": "string",
  "permissionLevel": "string",
  "email": "string",
  "qqNumber": "string",
  "mai2Name": "string",
  "mai2SHA256": "string",
  "botToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|username|string|true|none||none|
|permissionLevel|string|true|none||none|
|email|string|true|none||none|
|qqNumber|string|true|none||none|
|mai2Name|string|true|none||none|
|mai2SHA256|string|true|none||none|
|botToken|string|true|none||none|

<h2 id="tocS_FinalResponseVOUserResponseVO">FinalResponseVOUserResponseVO</h2>

<a id="schemafinalresponsevouserresponsevo"></a>
<a id="schema_FinalResponseVOUserResponseVO"></a>
<a id="tocSfinalresponsevouserresponsevo"></a>
<a id="tocsfinalresponsevouserresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "username": "string",
    "permissionLevel": "string",
    "email": "string",
    "qqNumber": "string",
    "mai2Name": "string",
    "mai2SHA256": "string",
    "botToken": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[UserResponseVO](#schemauserresponsevo)|false|none||none|

<h2 id="tocS_RegisterSecondStepsValidRequestVO">RegisterSecondStepsValidRequestVO</h2>

<a id="schemaregistersecondstepsvalidrequestvo"></a>
<a id="schema_RegisterSecondStepsValidRequestVO"></a>
<a id="tocSregistersecondstepsvalidrequestvo"></a>
<a id="tocsregistersecondstepsvalidrequestvo"></a>

```json
{
  "email": "string",
  "qqNumber": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|email|string|true|none||none|
|qqNumber|string|true|none||none|

<h2 id="tocS_RegisterUsernameValidRequestVO">RegisterUsernameValidRequestVO</h2>

<a id="schemaregisterusernamevalidrequestvo"></a>
<a id="schema_RegisterUsernameValidRequestVO"></a>
<a id="tocSregisterusernamevalidrequestvo"></a>
<a id="tocsregisterusernamevalidrequestvo"></a>

```json
{
  "username": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|username|string|true|none||none|

<h2 id="tocS_LoginResponseVO">LoginResponseVO</h2>

<a id="schemaloginresponsevo"></a>
<a id="schema_LoginResponseVO"></a>
<a id="tocSloginresponsevo"></a>
<a id="tocsloginresponsevo"></a>

```json
{
  "token": "string",
  "refreshToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|refreshToken|string|true|none||none|

<h2 id="tocS_FinalResponseVOLoginResponseVO">FinalResponseVOLoginResponseVO</h2>

<a id="schemafinalresponsevologinresponsevo"></a>
<a id="schema_FinalResponseVOLoginResponseVO"></a>
<a id="tocSfinalresponsevologinresponsevo"></a>
<a id="tocsfinalresponsevologinresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "token": "string",
    "refreshToken": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[LoginResponseVO](#schemaloginresponsevo)|false|none||none|

<h2 id="tocS_LoginRequestVO">LoginRequestVO</h2>

<a id="schemaloginrequestvo"></a>
<a id="schema_LoginRequestVO"></a>
<a id="tocSloginrequestvo"></a>
<a id="tocsloginrequestvo"></a>

```json
{
  "username": "string",
  "password": "string",
  "captchaToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|username|string|true|none||none|
|password|string|true|none||none|
|captchaToken|string|true|none||none|

<h2 id="tocS_LogoutRequestVO">LogoutRequestVO</h2>

<a id="schemalogoutrequestvo"></a>
<a id="schema_LogoutRequestVO"></a>
<a id="tocSlogoutrequestvo"></a>
<a id="tocslogoutrequestvo"></a>

```json
{
  "token": "string",
  "refreshToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|refreshToken|string|true|none||none|

<h2 id="tocS_RefreshTokenRequestVO">RefreshTokenRequestVO</h2>

<a id="schemarefreshtokenrequestvo"></a>
<a id="schema_RefreshTokenRequestVO"></a>
<a id="tocSrefreshtokenrequestvo"></a>
<a id="tocsrefreshtokenrequestvo"></a>

```json
{
  "refreshToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|refreshToken|string|true|none||none|

<h2 id="tocS_RegisterVerifyRequestVO">RegisterVerifyRequestVO</h2>

<a id="schemaregisterverifyrequestvo"></a>
<a id="schema_RegisterVerifyRequestVO"></a>
<a id="tocSregisterverifyrequestvo"></a>
<a id="tocsregisterverifyrequestvo"></a>

```json
{
  "token": "string",
  "valid": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|valid|string|true|none||none|

<h2 id="tocS_RegisterResponseVO">RegisterResponseVO</h2>

<a id="schemaregisterresponsevo"></a>
<a id="schema_RegisterResponseVO"></a>
<a id="tocSregisterresponsevo"></a>
<a id="tocsregisterresponsevo"></a>

```json
{
  "msg": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|msg|string|true|none||none|

<h2 id="tocS_FinalResponseVORegisterResponseVO">FinalResponseVORegisterResponseVO</h2>

<a id="schemafinalresponsevoregisterresponsevo"></a>
<a id="schema_FinalResponseVORegisterResponseVO"></a>
<a id="tocSfinalresponsevoregisterresponsevo"></a>
<a id="tocsfinalresponsevoregisterresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "msg": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[RegisterResponseVO](#schemaregisterresponsevo)|false|none||none|

<h2 id="tocS_RegisterRequestVO">RegisterRequestVO</h2>

<a id="schemaregisterrequestvo"></a>
<a id="schema_RegisterRequestVO"></a>
<a id="tocSregisterrequestvo"></a>
<a id="tocsregisterrequestvo"></a>

```json
{
  "username": "string",
  "password": "string",
  "email": "string",
  "qqNumber": "string",
  "weChatID": "string",
  "captchaToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|username|string|true|none||none|
|password|string|true|none||none|
|email|string|true|none||none|
|qqNumber|string|true|none||none|
|weChatID|string|true|none||none|
|captchaToken|string|true|none||none|

<h2 id="tocS_ResetPasswordIsValidRequestVO">ResetPasswordIsValidRequestVO</h2>

<a id="schemaresetpasswordisvalidrequestvo"></a>
<a id="schema_ResetPasswordIsValidRequestVO"></a>
<a id="tocSresetpasswordisvalidrequestvo"></a>
<a id="tocsresetpasswordisvalidrequestvo"></a>

```json
{
  "token": "string",
  "valid": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|valid|string|true|none||none|

<h2 id="tocS_ResetPasswordValidRequestVO">ResetPasswordValidRequestVO</h2>

<a id="schemaresetpasswordvalidrequestvo"></a>
<a id="schema_ResetPasswordValidRequestVO"></a>
<a id="tocSresetpasswordvalidrequestvo"></a>
<a id="tocsresetpasswordvalidrequestvo"></a>

```json
{
  "token": "string",
  "valid": "string",
  "password": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|
|valid|string|true|none||none|
|password|string|true|none||none|

<h2 id="tocS_Null">Null</h2>

<a id="schemanull"></a>
<a id="schema_Null"></a>
<a id="tocSnull"></a>
<a id="tocsnull"></a>

```json
{}

```

### 属性

*None*

<h2 id="tocS_FinalResponseVONull">FinalResponseVONull</h2>

<a id="schemafinalresponsevonull"></a>
<a id="schema_FinalResponseVONull"></a>
<a id="tocSfinalresponsevonull"></a>
<a id="tocsfinalresponsevonull"></a>

```json
{
  "isSuccess": true,
  "data": {}
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[Null](#schemanull)|false|none||none|

<h2 id="tocS_ResetPasswordRequestVO">ResetPasswordRequestVO</h2>

<a id="schemaresetpasswordrequestvo"></a>
<a id="schema_ResetPasswordRequestVO"></a>
<a id="tocSresetpasswordrequestvo"></a>
<a id="tocsresetpasswordrequestvo"></a>

```json
{
  "email": "string",
  "captchaToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|email|string|true|none||none|
|captchaToken|string|true|none||none|

<h2 id="tocS_RefreshTokenResponseVO">RefreshTokenResponseVO</h2>

<a id="schemarefreshtokenresponsevo"></a>
<a id="schema_RefreshTokenResponseVO"></a>
<a id="tocSrefreshtokenresponsevo"></a>
<a id="tocsrefreshtokenresponsevo"></a>

```json
{
  "token": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|

<h2 id="tocS_FinalResponseVORefreshTokenResponseVO">FinalResponseVORefreshTokenResponseVO</h2>

<a id="schemafinalresponsevorefreshtokenresponsevo"></a>
<a id="schema_FinalResponseVORefreshTokenResponseVO"></a>
<a id="tocSfinalresponsevorefreshtokenresponsevo"></a>
<a id="tocsfinalresponsevorefreshtokenresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "token": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[RefreshTokenResponseVO](#schemarefreshtokenresponsevo)|false|none||none|

<h2 id="tocS_TokenValidationRequestVO">TokenValidationRequestVO</h2>

<a id="schematokenvalidationrequestvo"></a>
<a id="schema_TokenValidationRequestVO"></a>
<a id="tocStokenvalidationrequestvo"></a>
<a id="tocstokenvalidationrequestvo"></a>

```json
{
  "token": "string",
  "refreshToken": "string",
  "botToken": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|false|none||none|
|refreshToken|string|false|none||none|
|botToken|string|false|none||none|

<h2 id="tocS_FinalResponseVOBotBindResponseVO">FinalResponseVOBotBindResponseVO</h2>

<a id="schemafinalresponsevobotbindresponsevo"></a>
<a id="schema_FinalResponseVOBotBindResponseVO"></a>
<a id="tocSfinalresponsevobotbindresponsevo"></a>
<a id="tocsfinalresponsevobotbindresponsevo"></a>

```json
{
  "isSuccess": true,
  "data": {
    "botKey": "string"
  }
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|[BotBindResponseVO](#schemabotbindresponsevo)|false|none||none|

<h2 id="tocS_BotBindResponseVO">BotBindResponseVO</h2>

<a id="schemabotbindresponsevo"></a>
<a id="schema_BotBindResponseVO"></a>
<a id="tocSbotbindresponsevo"></a>
<a id="tocsbotbindresponsevo"></a>

```json
{
  "botKey": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botKey|string|true|none||none|

<h2 id="tocS_BotBindRequestVO">BotBindRequestVO</h2>

<a id="schemabotbindrequestvo"></a>
<a id="schema_BotBindRequestVO"></a>
<a id="tocSbotbindrequestvo"></a>
<a id="tocsbotbindrequestvo"></a>

```json
{
  "botToken": "string",
  "botName": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botToken|string|true|none||none|
|botName|string|true|none||none|

<h2 id="tocS_BotUnbindRequestVO">BotUnbindRequestVO</h2>

<a id="schemabotunbindrequestvo"></a>
<a id="schema_BotUnbindRequestVO"></a>
<a id="tocSbotunbindrequestvo"></a>
<a id="tocsbotunbindrequestvo"></a>

```json
{
  "botKey": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botKey|string|true|none||none|

<h2 id="tocS_FinalResponseVOString">FinalResponseVOString</h2>

<a id="schemafinalresponsevostring"></a>
<a id="schema_FinalResponseVOString"></a>
<a id="tocSfinalresponsevostring"></a>
<a id="tocsfinalresponsevostring"></a>

```json
{
  "isSuccess": true,
  "data": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isSuccess|boolean|true|none||none|
|data|string|false|none||none|

<h2 id="tocS_PermissionRequestVO">PermissionRequestVO</h2>

<a id="schemapermissionrequestvo"></a>
<a id="schema_PermissionRequestVO"></a>
<a id="tocSpermissionrequestvo"></a>
<a id="tocspermissionrequestvo"></a>

```json
{
  "changeUsername": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|changeUsername|string|true|none||none|

<h2 id="tocS_PhotoFavoriteRequestVO">PhotoFavoriteRequestVO</h2>

<a id="schemaphotofavoriterequestvo"></a>
<a id="schema_PhotoFavoriteRequestVO"></a>
<a id="tocSphotofavoriterequestvo"></a>
<a id="tocsphotofavoriterequestvo"></a>

```json
{
  "photoUUID": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoUUID|string|true|none||none|

<h2 id="tocS_TurboTicketWhitelistRequestVO">TurboTicketWhitelistRequestVO</h2>

<a id="schematurboticketwhitelistrequestvo"></a>
<a id="schema_TurboTicketWhitelistRequestVO"></a>
<a id="tocSturboticketwhitelistrequestvo"></a>
<a id="tocsturboticketwhitelistrequestvo"></a>

```json
{
  "ticketId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||none|

<h2 id="tocS_TurboCustomNameRequestVO">TurboCustomNameRequestVO</h2>

<a id="schematurbocustomnamerequestvo"></a>
<a id="schema_TurboCustomNameRequestVO"></a>
<a id="tocSturbocustomnamerequestvo"></a>
<a id="tocsturbocustomnamerequestvo"></a>

```json
{
  "turboName": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||none|

<h2 id="tocS_Unit">Unit</h2>

<a id="schemaunit"></a>
<a id="schema_Unit"></a>
<a id="tocSunit"></a>
<a id="tocsunit"></a>

```json
{}

```

### 属性

*None*

<h2 id="tocS_UpsertUserPortraitRequestVO">UpsertUserPortraitRequestVO</h2>

<a id="schemaupsertuserportraitrequestvo"></a>
<a id="schema_UpsertUserPortraitRequestVO"></a>
<a id="tocSupsertuserportraitrequestvo"></a>
<a id="tocsupsertuserportraitrequestvo"></a>

```json
{
  "divData": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|divData|string|true|none||none|

