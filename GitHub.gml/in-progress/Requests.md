# Requests
There are two request structures that are created when you make a request to an endpoint, one for HTTP requests and one for GitHub specific requests. The HTTP request is created when any `HTTP*` constructor is called, and it stores information about that specific request. A GitHub request is slightly different and handles GitHub specific requests.

All requests made through this API are stored globally and processed when a HTTP async event is fired. Header data structures are automatically deleted and you can let the garbage collector deal with the rest of the structure.

## HTTP Request
When any `HTTP*` request is called, a HTTP structure will be created. This structure contains the following data.

| Property | Type | Description |
| --- | --- | --- |
| `requestID` | `Real` | The GameMaker request ID used for processing in the HTTP async event. |
| `status` | `Real` | Mirrors GameMakers `async_load[? "status"]`. |
| `result` | `String` | The result of the request, the returning body plaintext. |
| `requestURL` | `String` | The URL of the request. |
| `httpStatus` | `Real` | The HTTP status of the request, until it's processed this will be `undefined`. |
| `headerMap` | `ID.DSMap` | The `ds_map` ID of the current request. This is automatically deleted upon request completion. |
| `requestBody` | `String` | The body of the request. |
| `requestMethod` | `String` | The request method. |
| `localTarget` | `String` | Local filepath target for downloading files. |
| `contentLength` | `Real` | The content length of data that is being downloaded / uploaded. |
| `sizeDownloaded` | `Real` | The size of the content that has currently been downloaded. |

## GitHub Request
When any GitHub request is called, a GitHub structure will be created. This structure contains the following data.

| Property | Type | Description |
| --- | --- | --- |
| `requestID` | `Real` | The GameMaker request ID used for processing in the HTTP async event. |
| `status` | `Real` | Mirrors GameMakers `async_load[? "status"]`. |
| `httpStatus` | `Real` | The HTTP status of the request, until it's processed this will be `undefined`. |
| `contentLength` | `Real` | The content length of data that is being downloaded / uploaded. |
| `sizeDownloaded` | `Real` | The size of the content that has currently been downloaded. |
| `result` | `Struct` | The resulting decoded data from the request. |

?> If data is being uploaded via any HTTP request method, GameMaker does not return a `size_uploaded` value, so you will not be able to get the status of the current upload and just have to hope and pray that it successfully goes through. The GitHub API will provide a response once an update is completed.