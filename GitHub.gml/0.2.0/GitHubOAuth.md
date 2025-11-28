# GitHubOAuth

`new GitHubOAuth(clientID, [clientSecret]);`

<!-- tabs:start -->

#### **Description**

`Returns` - `Struct.GitHubOAuth`.

| Name | Type | Description |
| --- | --- | --- |
| `clientID` | `String` | The client ID to use for authentication. |
| `[clientSecret]` | `String` | The client secret to use for web-flow authentication. |

Constructor for creating a new instance of GitHubOAuth.

#### **Example**

```gml
oauth = new GitHubOAuth(_clientID, _clientSecret);
```

<!-- tabs:end -->

## requestAuthenticationViaWebPage
`GitHubOAuth.requestAuthenticationViaWebPage(scope, [expireTime]);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `scope` | `Array.String` | An array of authentication [scopes](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes). |
| `[expireTime]` | `Real` | Expiry time in seconds to allow the authentication request to expire. |

Request OAuth user authentication via a web page.

#### **Example**

```gml
oauth.requestAuthenticationViaWebPage([ "repo", "read:user", ], 900);
```

<!-- tabs:end -->

## requestAuthentication
`GitHubOAuth.requestAuthentication(scope);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `scope` | `Array.String` | An array of authentication scopes. |

Request OAuth user authentication via the device flow.

#### **Example**

```gml
var _request = oauth.requestAuthenticationViaWebPage([ "repo", "read:user", ]);
```

<!-- tabs:end -->

## pollAuthentication
`GitHubOAuth.pollAuthentication(deviceCode, interval, [maxAttempts]);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `deviceCode` | `String` | The device code that was returned back from `requestAuthentication`. |
| `interval` | `Real` | The interval in seconds to poll the authentication. |
| `[expireTime]` | `Real` | The time in seconds in which the current authentication device code will expire. |
| `[maxAttempts]` | `Real` | The maximum number of attempts to make to poll the authentication. |

Start polling the authentication to check if the user as granted it.

#### **Example**

```gml
oauth.pollAuthentication(_deviceCode, _interval, _expireTime, 20);
```

<!-- tabs:end -->

## cancelAuthentication
`GitHubOAuth.cancelAuthentication();`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

Cancels the current authentication request.

#### **Example**

```gml
oauth.cancelAuthentication();
```

<!-- tabs:end -->

## hasActiveRequest
`GitHubOAuth.hasActiveRequest();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Bool`.

Returns if there is an active authentication request in-progress. GitHub.gml only allows one authentication request at a time, this is useful to check if there is one still running before starting another request.

#### **Example**

```gml
var _hasActiveRequest = oauth.hasActiveRequest();
```

<!-- tabs:end -->

## setAuthenticationCallback
`GitHubOAuth.setAuthenticationCallback(callback);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `callback` | `Function` | The method to execute. |

Set the authentication callback which will be executed when the authentication is successful.

#### **Example**

```gml
oauth.setAuthenticationCallback(_myCallbackFunction);
```

<!-- tabs:end -->

## setAuthenticationErrorback
`GitHubOAuth.setAuthenticationErrorback(callback);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `callback` | `Function` | The method to execute. |

Set the authentication errorback which will be executed when the authentication is unsuccessful.

#### **Example**

```gml
oauth.setAuthenticationErrorback(_myErrorbackFunction);
```

<!-- tabs:end -->

## setAuthenticationTimeoutCallback
`GitHubOAuth.setAuthenticationTimeoutCallback(callback);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `callback` | `Function` | The method to execute. |

Set the authentication callback which will be executed when the authentication times out.

#### **Example**

```gml
oauth.setAuthenticationTimeoutCallback(_myCallbackFunction);
```

<!-- tabs:end -->

## hasAuthentication
`GitHubOAuth.hasAuthentication();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Bool`.

Returns wether we have user authentication or not.

#### **Example**

```gml
var _userHasAuthentication = oauth.hasAuthentication();
```

<!-- tabs:end -->

## getAuthenticationToken
`GitHubOAuth.getAuthenticationToken();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token.

#### **Example**

```gml
var _userAuthenticationToken = oauth.hasAuthentication();
```

<!-- tabs:end -->

## getAuthenticationTokenType
`GitHubOAuth.getAuthenticationTokenType();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token type.

#### **Example**

```gml
var _userAuthenticationTokenType = oauth.getAuthenticationTokenType();
```

<!-- tabs:end -->

## getAuthenticationTokenScope
`GitHubOAuth.getAuthenticationTokenScope();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token [scope](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes).

#### **Example**

```gml
var _userAuthenticationTokenScope = oauth.getAuthenticationTokenScope();
```

<!-- tabs:end -->

## setAuthenticationSuccessHTML
`GitHubOAuth.setAuthenticationSuccessHTML(html);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `html` | `String` | The HTML to use. |

Set the web-flow success HTML which will be displayed in the browser when authentication is successful.

#### **Example**

```gml
oauth.setAuthenticationSuccessHTML(_html);
```

<!-- tabs:end -->

## setAuthenticationErrorHTML
`GitHubOAuth.setAuthenticationErrorHTML(html);`

<!-- tabs:start -->

#### **Description**

`Returns` - `N/A`.

| Name | Type | Description |
| --- | --- | --- |
| `html` | `String` | The HTML to use. |

Set the web-flow error HTML which will be displayed in the browser when authentication is unsuccessful.

#### **Example**

```gml
oauth.setAuthenticationErrorHTML(_html);
```

<!-- tabs:end -->