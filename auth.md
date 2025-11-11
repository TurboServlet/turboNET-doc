# 认证相关API

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