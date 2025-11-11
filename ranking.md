# 排行榜相关API

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