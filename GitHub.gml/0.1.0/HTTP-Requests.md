# HTTP API Reference
Below is a reference to the built-in HTTP API. These are used to make generic HTTP requests using the same system as the rest of GitHub.gml. They can be used outside of GitHub.gml if you require to make a generic request to somewhere other than GitHub.

## HTTPRequest
`new HTTPRequest(requestURL, requestMethod, headerMap, requestBody);`

<!-- tabs:start -->

#### **Description**

`Returns` - [HTTP request constructor](Requests#http-request).

| Name | Type | Description |
| --- | --- | --- |
| `requestURL` | `String` | The URL of the outgoing request. |
| `requestMethod` | `String` | The method of the outgoing request (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`). |
| `headerMap` | `ID.DSMap` | The request headers in the form of a DSMap. Automatically cleaned up when processed. |
| `requestBody` | `String` | The body of the outgoing request. |

Creates a new generic HTTP request.

#### **Example**
Create:
```gml
// Create header map
var _headerMap = ds_map_create();
ds_map_add(_headerMap, "User-Agent", "GameMaker");

// Create request
request = new HTTPRequest("https://www.google.com/", "GET", "");
```

Step:
```gml
if (request.httpStatus == 200)
{
    show_message(request.result);
}
```

<!-- tabs:end -->

## HTTPGet
`new HTTPGet(requestURL);`

<!-- tabs:start -->

#### **Description**

`Returns` - [HTTP request constructor](Requests#http-request).

| Name | Type | Description |
| --- | --- | --- |
| `requestURL` | `String` | The URL of the outgoing request. |

Creates a new generic HTTP get request.

#### **Example**
Create:
```gml
// Create request
request = new HTTPGet("https://www.google.com/");
```

Step:
```gml
if (request.httpStatus == 200)
{
    show_message(request.result);
}
```

<!-- tabs:end -->

## HTTPGetFile
`new HTTPGetFile(requestURL, localTarget);`

<!-- tabs:start -->

#### **Description**

`Returns` - [HTTP request constructor](Requests#http-request).

| Name | Type | Description |
| --- | --- | --- |
| `requestURL` | `String` | The URL of the outgoing request. |
| `localTarget` | `String` | The filepath target of the download request. |

Creates a new generic HTTP get file request to download a file to a given target location.

#### **Example**
Create:
```gml
// Create request
request = new HTTPGetFile("https://example.com/assets/myImage.png", "images/myImage.png");
```

Step:
```gml
// We can check the status to see if the file is still being downloaded.
if (request.status == 1)
{
    // If the status is equal to 1, we can display the downloaded size vs the content length.
    show_debug_message($"Downloaded {request.sizeDownloaded}B of {request.contentLength}B");
}
else if (request.status == 0)
{
    show_message("File successfully downloaded!");
}
```

<!-- tabs:end -->