# 照片相关API

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