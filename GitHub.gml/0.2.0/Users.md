# Users

## getAuthenticatedUser
`GitHub.getAuthenticatedUser();`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

Get the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#get-the-authenticated-user).

#### **Example**

```gml
var _currentUser = github.getAuthenticatedUser();
```

<!-- tabs:end -->

## updateAuthenticatedUser
`GitHub.updateAuthenticatedUser([name], [email], [blog], [twitterUsername], [company], [location], [hireable], [bio]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[user]` | `String` | The new name of the user. |
| `[email]` | `String` | The new email of the user. |
| `[blog]` | `String` | The new blog URL of the user. |
| `[twitterUsername]` | `String` | The new twitter (X) username of the user. |
| `[company]` | `String` | The new company of the user. |
| `[location]` | `String` | The new location of the user. |
| `[hireable]` | `Bool` | The new hiring availability of the user. |
| `[bio]` | `String` | The new bio of the user. |

Update the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#update-the-authenticated-user).

#### **Example**

```gml
github.updateAuthenticatedUser("I changed my name", "mynewemail@emails.com", "mynewblog@blog.com", "WhoUsesTwitter", "My Company", "Sahara Desert", false, "Hello GitHub");
```

<!-- tabs:end -->

## getUserByID
`GitHub.getUserByID(accountID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `accountID` | `Real` | The users account ID. |

Get a user by their account ID.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#get-a-user-using-their-id).

#### **Example**

```gml
var _user = github.getUserByID(98592845);
```

<!-- tabs:end -->

## getUsers
`GitHub.getUsers([since], [perPage]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[since]` | `Real` | A user ID. Only return users with an ID greater than this ID. |
| `[perPage]` | `Real` | The number of results per page (max 100). |

Get a list of users.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#list-users).

#### **Example**

```gml
var _users = github.getUsers(484, 20);
```

<!-- tabs:end -->

## getUser
`GitHub.getUser(username);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The users username. |

Get a user by their username.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#get-a-user).

#### **Example**

```gml
var _user = github.getUser("AlubJ");
```

<!-- tabs:end -->

## getUserHovercard
`GitHub.getUserHovercard(username, [subjectType], [subjectID]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The users username. |
| `[subjectType]` | `String` | Identifies which additional information you'd like to receive about the person's hovercard. Can be "organization", "repository", "issue", "pull_request". Required when using subjectID. |
| `[subjectID]` | `String` | Uses the ID for the subjectType you specified. Required when using subjectType. |

Get contextual information about a user.

[GitHub Documentation](https://docs.github.com/en/rest/users/users#get-contextual-information-for-a-user).

#### **Example**

```gml
var _userHovercard = github.getUserHovercard("AlubJ", "repository", "GitHub.gml");
```

<!-- tabs:end -->