# Turbo盒子工具相关API

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