# 权限管理相关API

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