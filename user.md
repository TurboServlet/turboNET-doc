# 用户相关API

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