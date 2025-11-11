# Bot管理相关API

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