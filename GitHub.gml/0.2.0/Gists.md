# Gists

## getGistsCreatedByMe
`GitHub.getGistsCreatedByMe([since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get all the gists created by the authenticated user, if no authorization is provided it returns all public gists.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-gists-for-the-authenticated-user).

#### **Example**

```gml
request = github.getGistsCreatedByMe(undefined, 10, 1);
```

<!-- tabs:end -->

## createGist
`GitHub.createGist(gist);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gist` | `Struct.GitHubGist` | The gist struct. |

Create a new gist to the currently authorized user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#create-a-gist).

#### **Example**

```gml
// Create a new gist
var _gist = new GitHubGist("I created this in GameMaker", false);
_gist.addFile("test.txt", "This is a test of GitHub.gml");

// Send request
request = github.createGist(_gist);
```

<!-- tabs:end -->

## getPublicGists
`GitHub.getPublicGists([since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a list of public gists.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-public-gists).

#### **Example**

```gml
request = github.getPublicGists(undefined, 10, 1);
```

<!-- tabs:end -->

## getStarredGists
`GitHub.getStarredGists([since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a list of gists starred by the authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-starred-gists).

#### **Example**

```gml
request = github.getStarredGists(undefined, 10, 1);
```

<!-- tabs:end -->

## getGist
`GitHub.getGist(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Get a gist from a gist ID.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#get-a-gist).

#### **Example**

```gml
request = github.getGist("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## updateGist
`GitHub.updateGist(gistID, gist);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `gist` | `Struct.GitHubGist` | The gist struct. |

Update a gist that's owned by the current authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#update-a-gist).

#### **Example**

```gml
// Create a new gist
var _gist = new GitHubGist("I created this in GameMaker", false);
_gist.addFile("test.txt", "This is a test of GitHub.gml (with some new content)", "changedname.txt");

// Update request
request = github.updateGist("aa5a315d61ae9438b18d", _gist);
```

<!-- tabs:end -->

## deleteGist
`GitHub.deleteGist(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Delete a gist that's owned by the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#delete-a-gist).

#### **Example**

```gml
request = github.deleteGist("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## getGistCommits
`GitHub.getGistCommits(gistID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a gists commits from a gist ID.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-gist-commits).

#### **Example**

```gml
request = github.getGistCommits("aa5a315d61ae9438b18d", 10, 1);
```

<!-- tabs:end -->

## getGistForks
`GitHub.getGistForks(gistID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a gists forks from a gist ID.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-gist-forks).

#### **Example**

```gml
request = github.getGistForks("aa5a315d61ae9438b18d", 10, 1);
```

<!-- tabs:end -->

## forkGist
`GitHub.forkGist(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Fork a gist from a gist ID.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#fork-a-gist).

#### **Example**

```gml
request = github.forkGist("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## isGistStarred
`GitHub.isGistStarred(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Check if a gist is starred by the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#check-if-a-gist-is-starred).

#### **Example**

```gml
request = github.isGistStarred("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## starGist
`GitHub.starGist(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Star a gist by the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#star-a-gist).

#### **Example**

```gml
request = github.starGist("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## unstarGist
`GitHub.unstarGist(gistID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |

Unstar a gist by the currently authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#unstar-a-gist).

#### **Example**

```gml
request = github.starGist("aa5a315d61ae9438b18d");
```

<!-- tabs:end -->

## getGistRevision
`GitHub.getGistRevision(gistID, sha);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `sha` | `String` | The sha of the gist. |

Get a gist revision from the gist ID and sha

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#get-a-gist-revision).

#### **Example**

```gml
request = github.getGistRevision("aa5a315d61ae9438b18d", "5bd05e06af7e2cef6c90ab2c4538e60f7e160bab493dba415e40417807140356");
```

<!-- tabs:end -->

## getUserGists
`GitHub.getUserGists(user, [since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `user` | `String` | The username of the user to search. |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a list of gists by a given user.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#list-gists-for-a-user).

#### **Example**

```gml
request = github.getUserGists("AlubJ", undefined, 10, 1);
```

<!-- tabs:end -->