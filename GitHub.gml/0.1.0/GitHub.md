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