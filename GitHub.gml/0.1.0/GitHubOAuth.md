# GitHubOAuth

`new GitHubOAuth(clientID);`

<!-- tabs:start -->

#### **Description**

`Returns` - `Struct.GitHubOAuth`.

| Name | Type | Description |
| --- | --- | --- |
| `_clientID` | `String` | The client ID to use for authentication. |

Constructor for creating a new instance of GitHubOAuth.

#### **Example**

```gml
oauth = new GitHubOAuth(_clientID);
```

<!-- tabs:end -->

## requestAuthentication
`GitHubOAuth.requestAuthentication(scope);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `scope` | `Array.String` | An array of authentication [scopes](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/scopes-for-oauth-apps). |

Request OAuth user authentication.

#### **Example**

```gml
oauth.requestAuthentication([ "repo", "read:user" ]);
```

<!-- tabs:end -->

## pollAuthentication
`GitHubOAuth.pollAuthentication(deviceCode, interval, [maxAttempts]);`

<!-- tabs:start -->

#### **Description**

`Returns` - N/A.

| Name | Type | Description |
| --- | --- | --- |
| `deviceCode` | `String` | The device code that was returned back from `requestAuthentication`. |
| `interval` | `Real` | The interval in seconds to poll the authentication. |
| `[maxAttempts]` | `Real` | The maximum number of attempts to make to poll the authentication. |

Start polling the authentication to check if the user as granted it. Only call this function once.

?> Keep the interval time at or above the interval time that GitHub returns back upon requesting authentication. GitHub will rate limit if requests are sent out too quickly. I recommend you use the interval time that GitHub gives you and add a couple more second to it.

#### **Example**

```gml
oauth.requestAuthentication(_deviceCode, _interval, 20);
```

<!-- tabs:end -->

## setAuthenticationCallback
`GitHubOAuth.setAuthenticationCallback(callback);`

<!-- tabs:start -->

#### **Description**

`Returns` - N/A.

| Name | Type | Description |
| --- | --- | --- |
| `callback` | `Function` | The method to execute. |

Set the authentication callback which will be executed when the authentication is successful.

#### **Example**

```gml
oauth.setAuthenticationCallback(_method);
```

<!-- tabs:end -->

## getAuthenticationToken
`GitHubOAuth.getAuthenticationToken();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token. Returns `undefined` if no authentication has been granted.

#### **Example**

```gml
oauth.getAuthenticationToken();
```

<!-- tabs:end -->

## getAuthenticationTokenType
`GitHubOAuth.getAuthenticationTokenType();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token type. Returns `undefined` if no authentication has been granted.

#### **Example**

```gml
oauth.getAuthenticationTokenType();
```

<!-- tabs:end -->

## getAuthenticationTokenScope
`GitHubOAuth.getAuthenticationTokenScope();`

<!-- tabs:start -->

#### **Description**

`Returns` - `String`.

Returns back the current authentication token scope. Returns `undefined` if no authentication has been granted.

#### **Example**

```gml
oauth.getAuthenticationTokenScope();
```

<!-- tabs:end -->