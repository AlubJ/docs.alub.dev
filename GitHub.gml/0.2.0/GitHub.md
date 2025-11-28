# GitHub

`new GitHub([authToken]);`

<!-- tabs:start -->

#### **Description**

`Returns` - `Struct.GitHub`.

| Name | Type | Description |
| --- | --- | --- |
| `[authToken]` | `String` | The authentication token to use. |

Constructor for creating a new instance of GitHub.

#### **Example**

```gml
github = new GitHub(_authToken);
```

<!-- tabs:end -->

## setAuthenticationToken
`GitHub.setAuthenticationToken(authToken);`

<!-- tabs:start -->

#### **Description**

`Returns` - N/A.

| Name | Type | Description |
| --- | --- | --- |
| `authToken` | `String` | The authentication token to use. |

Set the authentication token, useful if requesting authentication from a user.

#### **Example**

```gml
github.setAuthenticationToken(_authToken);
```

<!-- tabs:end -->

## getRateLimitLimit
`GitHub.getRateLimitLimit();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Real`.

Get the current rate limit for the authenticated user, returns `undefined` when no requests have been made.

#### **Example**

```gml
var _rateLimit = github.getRateLimitLimit();
```

<!-- tabs:end -->

## getRateLimitUsed
`GitHub.getRateLimitUsed();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Real`.

Get the current used rate limit for the authenticated user, returns `undefined` when no requests have been made.

#### **Example**

```gml
var _rateLimitUsed = github.getRateLimitUsed();
```

<!-- tabs:end -->

## getRateLimitRemaining
`GitHub.getRateLimitRemaining();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Real`.

Get the current remaining rate limit for the authenticated user, returns `undefined` when no requests have been made.

#### **Example**

```gml
var _rateLimitRemaining = github.getRateLimitRemaining();
```

<!-- tabs:end -->

## getRateLimitReset
`GitHub.getRateLimitReset();`

<!-- tabs:start -->

#### **Description**

`Returns` - `Datetime`.

Get the current rate limit reset for the authenticated user, returns `undefined` when no requests have been made.

#### **Example**

```gml
var _rateLimitReset = github.getRateLimitReset();
```

<!-- tabs:end -->