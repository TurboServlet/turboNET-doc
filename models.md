# 数据模型

## FinalResponseVOListBotBindListResponseVO

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
|data|[[BotBindListResponseVO](#botbindlistresponsevo)]|false|none||none|

## BotBindListResponseVO

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

## FinalResponseVOPermissionEnum

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

### 枚举值

|属性|值|
|---|---|
|data|ADMIN|
|data|BUILDER|
|data|AUTHORIZER|
|data|USER|
|data|BANNED|

## QrResponseVO

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

## FinalResponseVOQrResponseVO

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
|data|[QrResponseVO](#qrresponsevo)|false|none||none|

## HomeResponseVO

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

## FinalResponseVOHomeResponseVO

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
|data|[HomeResponseVO](#homeresponsevo)|false|none||none|

## PacketResultHourDTO

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

## PacketResultBeforeDTO

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

## NetworkResponseVO

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
|packets|[PacketResultHourDTO](#packetresulthourdto)|true|none||none|
|packetsBefore|[PacketResultBeforeDTO](#packetresultbeforedto)|true|none||none|

## FinalResponseVONetworkResponseVO

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
|data|[NetworkResponseVO](#networkresponsevo)|false|none||none|

## PermissionResponseVO

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
|permissionList|[[PermissionListResponseVO](#permissionlistresponsevo)]|true|none||none|
|authorizationsList|[[AuthorizationResponseVO](#authorizationresponsevo)]|true|none||none|
|bannedList|[[BanResponseVO](#banresponsevo)]|true|none||none|

### 枚举值

|属性|值|
|---|---|
|permissionLevel|ADMIN|
|permissionLevel|BUILDER|
|permissionLevel|AUTHORIZER|
|permissionLevel|USER|
|permissionLevel|BANNED|

## PermissionListResponseVO

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

## FinalResponseVOPermissionResponseVO

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
|data|[PermissionResponseVO](#permissionresponsevo)|false|none||none|

## BanResponseVO

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

## AuthorizationResponseVO

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

### 枚举值

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

## SortObject

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

## PhotoResponseVO

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
|photoList|[PagePhotoListVO](#pagephotolistvo)|true|none||none|

## PhotoListVO

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

## PageableObject

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
|sort|[SortObject](#sortobject)|false|none||none|
|paged|boolean|false|none||none|
|pageNumber|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|unpaged|boolean|false|none||none|

## PagePhotoListVO

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
|content|[[PhotoListVO](#photolistvo)]|false|none||none|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#sortobject)|false|none||none|
|pageable|[PageableObject](#pageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|first|boolean|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

## FinalResponseVOPhotoResponseVO

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
|data|[PhotoResponseVO](#photoresponsevo)|false|none||none|

## UserInfoVO

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

## SyncVO

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

## PlayerDataResponseVO

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
|achievement|[AchievementVO](#achievementvo)|true|none||none|
|combo|[ComboVO](#combovo)|true|none||none|
|sync|[SyncVO](#syncvo)|true|none||none|
|userInfo|[UserInfoVO](#userinfovo)|true|none||none|
|allMusic|integer(int32)|true|none||none|

## FinalResponseVOPlayerDataResponseVO

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
|data|[PlayerDataResponseVO](#playerdataresponsevo)|false|none||none|

## ComboVO

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

## AchievementVO

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

## UserRanking

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

## SinglePlayerRanking

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

## RankingResponseVO

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
|singlePlayerRanking|[[SinglePlayerRanking](#singleplayerranking)]|true|none||none|
|userRanking|[UserRanking](#userranking)|true|none||none|
|totalPages|integer(int32)|true|none||none|
|totalElements|integer(int64)|true|none||none|

## FinalResponseVORankingResponseVO

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
|data|[RankingResponseVO](#rankingresponsevo)|false|none||none|

## UserAchievementRanking

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

## SinglePlayerAchievementRanking

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

## RankingAchievementResponseVO

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
|singlePlayerRanking|[[SinglePlayerAchievementRanking](#singleplayerachievementranking)]|true|none||none|
|userRanking|[UserAchievementRanking](#userachievementranking)|true|none||none|
|totalPages|integer(int32)|true|none||none|
|totalElements|integer(int64)|true|none||none|

## FinalResponseVORankingAchievementResponseVO

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
|data|[RankingAchievementResponseVO](#rankingachievementresponsevo)|false|none||none|

## UserInfo

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

## RecordResponseVO

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
|recordList|[[Mai2Record](#mai2record)]|true|none||none|

## NotesInfo

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

## MusicInfo

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

## Mai2Record

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
|userInfo|[UserInfo](#userinfo)|true|none||none|
|musicInfo|[MusicInfo](#musicinfo)|true|none||none|
|detailInfo|[DetailInfo](#detailinfo)|true|none||none|

## FinalResponseVORecordResponseVO

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
|data|[RecordResponseVO](#recordresponsevo)|false|none||none|

## DetailInfo

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
|tap|[NotesInfo](#notesinfo)|true|none||none|
|hold|[NotesInfo](#notesinfo)|true|none||none|
|slide|[NotesInfo](#notesinfo)|true|none||none|
|touch|[NotesInfo](#notesinfo)|true|none||none|
|mai2Break|[NotesInfo](#notesinfo)|true|none||none|

## TurboTicketInfoVO

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

## TicketVO

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

## TicketResponseVO

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
|ticketList|[[TicketVO](#ticketvo)]|true|none||none|
|turboTicketInfo|[TurboTicketInfoVO](#turboticketinfovo)|false|none||none|
|isEnableTurboTicket|boolean|true|none||none|
|isTicketEmpty|boolean|true|none||none|

## FinalResponseVOTicketResponseVO

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
|data|[TicketResponseVO](#ticketresponsevo)|false|none||none|

## TurboVO

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
|detail|[TurboDetailResponseVO](#turbodetailresponsevo)|true|none||none|

## TurboSingleDetailPlayerVO

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

## TurboResponseVO

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
|turboInfoList|[[TurboVO](#turbovo)]|true|none||none|

## TurboPlayDetailVO

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

## TurboDetailResponseVO

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
|tenMinutesDetail|[TurboPlayDetailVO](#turboplaydetailvo)|true|none||none|
|thirtyMinutesDetail|[TurboPlayDetailVO](#turboplaydetailvo)|true|none||none|
|hourDetail|[TurboPlayDetailVO](#turboplaydetailvo)|true|none||none|
|playerDetail|[[TurboSingleDetailPlayerVO](#turbosingledetailplayervo)]|true|none||none|

## FinalResponseVOTurboResponseVO

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
|data|[TurboResponseVO](#turboresponsevo)|false|none||none|

## UserResponseVO

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

## FinalResponseVOUserResponseVO

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
|data|[UserResponseVO](#userresponsevo)|false|none||none|

## RegisterSecondStepsValidRequestVO

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

## RegisterUsernameValidRequestVO

```json
{
  "username": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|username|string|true|none||none|

## LoginResponseVO

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

## FinalResponseVOLoginResponseVO

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
|data|[LoginResponseVO](#loginresponsevo)|false|none||none|

## LoginRequestVO

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

## LogoutRequestVO

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

## RefreshTokenRequestVO

```json
{
  "refreshToken": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|refreshToken|string|true|none||none|

## RegisterVerifyRequestVO

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

## RegisterResponseVO

```json
{
  "msg": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|msg|string|true|none||none|

## FinalResponseVORegisterResponseVO

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
|data|[RegisterResponseVO](#registerresponsevo)|false|none||none|

## RegisterRequestVO

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

## ResetPasswordIsValidRequestVO

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

## ResetPasswordValidRequestVO

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

## Null

```json
{}
```

### 属性

*None*

## FinalResponseVONull

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
|data|[Null](#null)|false|none||none|

## ResetPasswordRequestVO

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

## RefreshTokenResponseVO

```json
{
  "token": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string|true|none||none|

## FinalResponseVORefreshTokenResponseVO

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
|data|[RefreshTokenResponseVO](#refreshtokenresponsevo)|false|none||none|

## TokenValidationRequestVO

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

## FinalResponseVOBotBindResponseVO

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
|data|[BotBindResponseVO](#botbindresponsevo)|false|none||none|

## BotBindResponseVO

```json
{
  "botKey": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botKey|string|true|none||none|

## BotBindRequestVO

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

## BotUnbindRequestVO

```json
{
  "botKey": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|botKey|string|true|none||none|

## FinalResponseVOString

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

## PermissionRequestVO

```json
{
  "changeUsername": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|changeUsername|string|true|none||none|

## PhotoFavoriteRequestVO

```json
{
  "photoUUID": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|photoUUID|string|true|none||none|

## TurboTicketWhitelistRequestVO

```json
{
  "ticketId": 0
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ticketId|integer(int32)|true|none||none|

## TurboCustomNameRequestVO

```json
{
  "turboName": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|turboName|string|true|none||none|

## Unit

```json
{}
```

### 属性

*None*

## UpsertUserPortraitRequestVO

```json
{
  "divData": "string"
}
```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|divData|string|true|none||none|