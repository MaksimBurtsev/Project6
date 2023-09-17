# Задание №5. Знакомство с функционалом Swagger

## Activities

1. GET​/api​/v1​/Activities
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities]
- Заголовки запроса: -H  "accept: application/json; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-13T13:20:38.5561609+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-06-13T14:20:38.5561635+00:00",
    "completed": true
  }
```

2. POST​/api​/v1​/Activities
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 3,
  "title": "string",
  "dueDate": "2023-06-13T12:22:28.610Z"
  "completed": true
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
 {
  "id": 3,
  "title": "string",
  "dueDate": "2023-06-13T12:22:28.610Z"
  "completed": true
}
```

3. POST​/api​/v1​/Activities
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 700000000000000,
  "title": "string",
  "dueDate": "2023-06-13T12:22:28.610Z",
  "completed": true
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-cf0f00888b74494a891c28979a344883-3ccb45a7fde9904f-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 21."
    ]
  }
}
```

4. GET​/api​/v1​/Activities​/{12}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/12]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 12,
  "title": "Activity 12",
  "dueDate": "2023-06-14T00:51:44.1781316+00:00",
  "completed": true
}
```

5. GET​/api​/v1​/Activities​/{0}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/0]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 404
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-5476ff3a362ed44fb5d5d52f4dcd3dee-95e933654ee0e342-00"
}
```

6. PUT​/api​/v1​/Activities​/{4}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/4]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса:
```
{
  "id": 4,
  "title": "string",
  "dueDate": "2023-06-13T12:10:53.128Z",
  "completed": true
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 4,
  "title": "string",
  "dueDate": "2023-06-13T12:10:53.128Z",
  "completed": true
}
```

7. PUT​/api​/v1​/Activities​/{4000000000}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/4000000000]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса:
```
{
  "id": 4000000000,
  "title": "string",
  "dueDate": "2023-06-13T12:10:53.128Z",
  "completed": true
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-91cf4951954eef4abeea5e33befefe66-9df9b36565f9fe42-00",
  "errors": {
    "id": [
      "The value '4000000000' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 16."
    ]
  }
}
```

8. DELETE​/api​/v1​/Activities​/{7}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/7]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: отсутствует

9. DELETE​/api​/v1​/Activities​/{8888888888}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Activities/8888888888]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-825a1a9c9a627745bd2952e20d833cdf-7f15c670e663cb48-00",
  "errors": {
    "id": [
      "The value '8888888888' is not valid."
    ]
  }
}
```

## Authors

1. GET​/api​/v1​/Authors
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors]
- Заголовки запроса: -H  "accept: application/json; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  }
```

2. POST​/api​/v1​/Authors
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 2,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 2,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

3. POST​/api​/v1​/Authors
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 2000000000000,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-45744332e47a0c4481ccdfbec2305683-0d89f6dea3fe014d-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 19."
    ]
  }
}
```

4. GET​/api​/v1​/Authors​/authors​/books​/{30}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/30]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
    "id": 85,
    "idBook": 30,
    "firstName": "First Name 85",
    "lastName": "Last Name 85"
  },
  {
    "id": 86,
    "idBook": 30,
    "firstName": "First Name 86",
    "lastName": "Last Name 86"
  }
```

5. GET​/api​/v1​/Authors​/authors​/books​/{10101010101}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/10101010101]
- Заголовки запроса: -H  "accept: application/json; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5d5e7a8b6920694bb4774fb49ed181b4-ea219607f1c0b040-00",
  "errors": {
    "idBook": [
      "The value '10101010101' is not valid."
    ]
  }
}
```

6. GET​/api​/v1​/Authors​/{5}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/5]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 5,
  "idBook": 2,
  "firstName": "First Name 5",
  "lastName": "Last Name 5"
}
```

7. GET​/api​/v1​/Authors​/{555555}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/555555]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 404
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-9ccc1af8862746489a757b801fce1a9a-5b3d21afda58d943-00"
}
```

8. PUT​/api​/v1​/Authors​/{6}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/6]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 6,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 6,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

9. PUT​/api​/v1​/Authors​/{6000000000}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/6000000000]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" 
- Тело запроса: 
```
{
  "id": 6000000000,
  "idBook": 12,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-186b2f86caef7b4e88bf8b6b1e87f0c4-35427a9322f6cf4c-00",
  "errors": {
    "id": [
      "The value '6000000000' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 16."
    ]
  }
}
```

10. DELETE/api​/v1​/Authors​/{12}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/12]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: отсутствует

11. DELETE​/api​/v1​/Authors​/{121212121212}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Authors/121212121212]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6c102d2dfc68a244937499ad27c02522-774c792778dcf044-00",
  "errors": {
    "id": [
      "The value '121212121212' is not valid."
    ]
  }
}
```

## Books

1. GET​/api​/v1​/Books
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-12T13:46:59.6443406+00:00"
  }
```

2. POST​/api​/v1​/Books
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T09:07:25.188Z"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T13:47:26.342Z"
}
```

3. POST​/api​/v1​/Books
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 999999999999999999999999999999999999999999999,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T13:47:26.342Z"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-acc270362041a44895718d79bd7d9f62-174a1e2035458348-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 11."
    ]
  }
}
```

4. GET​/api​/v1​/Books​/{7}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books/7]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 7,
  "title": "Book 7",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 700,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-06T13:50:10.3953488+00:00"
}
```

5. GET​/api​/v1​/Books​/{7777777777}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books/7777777777]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-89bc2637615b784d90f2f1939854b7c2-f8f32cdb03b1c548-00",
  "errors": {
    "id": [
      "The value '7777777777' is not valid."
    ]
  }
}
```

6. PUT​/api​/v1​/Books​/{3}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books/3]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0" 
- Тело запроса: 
```
{
  "id": 3,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T13:51:02.755Z"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 3,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T13:51:02.755Z"
}
```

7. PUT​/api​/v1​/Books​/{3999999999}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books/3999999999]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 3999999999,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T13:51:02.755Z"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a89d90e8490a4a43b0cdb2e692d306c2-c0ce5e46d123314e-00",
  "errors": {
    "id": [
      "The value '3999999999' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 16."
    ]
  }
}
```

8. DELETE​/api​/v1​/Books​/{15}
- HTTP-DELETE;
- Полный URL запроса: [hhttps://fakerestapi.azurewebsites.net/api/v1/Books/15]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: отсутствует

9. DELETE​/api​/v1​/Books​/{15151515151}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Books/15151515151]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5f5c6fb36103a94f8436144051dc5428-36e5c38777d1e54b-00",
  "errors": {
    "id": [
      "The value '15151515151' is not valid."
    ]
  }
}
```

## CoverPhotos

1. GET​/api​/v1​/CoverPhotos
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  }
```

2. POST​/api​/v1​/CoverPhotos
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 4,
  "idBook": 0,
  "url": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 4,
  "idBook": 0,
  "url": "string"
}
```

3. POST​/api​/v1​/CoverPhotos
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 44444444444,
  "idBook": 0,
  "url": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-407666f543181446981919b08486ad83-b5ce87a144a1a943-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
4. GET​/api​/v1​/CoverPhotos​/books​/covers​/{8}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/8]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
[
  {
    "id": 8,
    "idBook": 8,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 8&w=250&h=350"
  }
]
```

5. GET​/api​/v1​/CoverPhotos​/books​/covers​/{8888888888}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/8888888888]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-543d36b630c3274387f678cd76675246-6939db1ebba8a444-00",
  "errors": {
    "idBook": [
      "The value '9999999999' is not valid."
    ]
  }
}
```

6. GET​/api​/v1​/CoverPhotos​/{19}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/19]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 19,
  "idBook": 19,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 19&w=250&h=350"
}
```

7. GET​/api​/v1​/CoverPhotos​/{0}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/0]
- Заголовки запроса: H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 404
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-559eb0f31495704d9bf7d2f65d75992e-0de7e021d3c44045-00"
}
```

8. PUT​//api/v1/CoverPhotos/{78}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/78]
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 78,
  "idBook": 0,
  "url": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 78,
  "idBook": 0,
  "url": "string"
}
```

9. PUT​//api/v1/CoverPhotos/{7877787878}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/7877787878]
- Заголовки запроса:  -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" 
- Тело запроса: 
```
{
  "id": 7877787878,
  "idBook": 0,
  "url": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a18542b36361954d9f9de0af329bcd76-992fdc14506ecf49-00",
  "errors": {
    "id": [
      "The value '7877788878' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 16."
    ]
  }
}
```

10. DELETE/api/v1/CoverPhotos/{24}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/24]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: отсутствует

11. DELETE/api/v1/CoverPhotos/{222222222222}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/222222222222]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-063f44f5a062f849a1ecfd4e8693a2f6-dd83bc540b016044-00",
  "errors": {
    "id": [
      "The value '222222222222' is not valid."
    ]
  }
}
```

## Users

1. GET/api/v1/Users
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users]
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
 {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
  {
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
  }
```

2. POST/api/v1/Users
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 66,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 66,
  "userName": "string",
  "password": "string"
}
```

3. POST/api/v1/Users
- HTTP-POST;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса: 
```
{
  "id": 3333333333,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-75ea2e0d598ffe4f95137c5820299f73-d9b7fc3e3a069545-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 16."
    ]
  }
}
```

4. GET​/api/v1/Users/{4}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/4]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 4,
  "userName": "User 4",
  "password": "Password4"
}
```

5. GET/api/v1/Users/{34}
- HTTP-GET;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/34]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 404
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-8e6802e9b754df48907ffbc20399c428-8bb71c66c4bec64d-00"
}
```

6. PUT​/api/v1/Users/{13}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/13]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса:
```
{
  "id": 13,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 200
- Тело ответа: 
```
{
  "id": 13,
  "userName": "string",
  "password": "string"
}
```

7. PUT/api/v1/Users/{12345678910}
- HTTP-PUT;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/12345678910}]
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса:
```
{
  "id": 12345678910,
   "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 400
- Тело ответа: 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-25c0c5ed0d200143a166b3738f4dafe3-803724e86d489b4a-00",
  "errors": {
    "id": [
      "The value '12345678910' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

8. DELETE/api/v1/Users/{7}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/7]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 200
- Тело ответа: отсутствует

9. DELETE/api/v1/Users/{7777777777}
- HTTP-DELETE;
- Полный URL запроса: [https://fakerestapi.azurewebsites.net/api/v1/Users/7777777777]
- Заголовки запроса: -H  "accept: */*"
- Тело запроса: отсутствует
- Статус-код ответа: 400
- Тело ответа:
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
   "traceId": "00-dce1733d11903c4e86c92feb05319891-746f4df8bd08c24c-00",
  "errors": {
    "id": [
      "The value '7777777777' is not valid."
    ]
  }
}
```



