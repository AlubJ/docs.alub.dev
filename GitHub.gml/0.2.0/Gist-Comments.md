# Gist Comments

## getGistComments
`GitHub.getGistComments(gistID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a list of a gists comments.

[GitHub Documentation](https://docs.github.com/en/rest/gists/comments#list-gist-comments).

#### **Example**

```gml
request = github.getGistComments("aa5a315d61ae9438b18d", 10, 1);
```

<!-- tabs:end -->

## createGistComment
`GitHub.createGistComment(gistID, body);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `Real` | The ID of the gist. |
| `body` | `String` | The body of the gist comment. |

Create an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/gists/comments#create-a-gist-comment).

#### **Example**

```gml
request = github.createGistComment("aa5a315d61ae9438b18d", "This is a cool gist");
```

<!-- tabs:end -->

## getGistComment
`GitHub.getGistComment(gistID, commentID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `commentID` | `Real` | The ID of the comment. |

Get a list of a gists comments.

[GitHub Documentation](https://docs.github.com/en/rest/gists/comments#get-a-gist-comment).

#### **Example**

```gml
request = github.getGistComment("aa5a315d61ae9438b18d", 1);
```

<!-- tabs:end -->

## updateGistComment
`GitHub.updateGistComment(gistID, commentID, body);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `Real` | The ID of the gist. |
| `commentID` | `Real` | The ID of the comment. |
| `body` | `String` | The body of the gist comment. |

Create an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/gists/comments#update-a-gist-comment).

#### **Example**

```gml
request = github.updateGistComment("aa5a315d61ae9438b18d", 1, "This is a new comment");
```

<!-- tabs:end -->

## deleteGistComment
`GitHub.deleteGistComment(gistID, commentID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `gistID` | `String` | The ID of the gist. |
| `commentID` | `Real` | The ID of the comment. |

Get a list of a gists comments.

[GitHub Documentation](https://docs.github.com/en/rest/gists/comments#delete-a-gist-comment).

#### **Example**

```gml
request = github.deleteGistComment("aa5a315d61ae9438b18d", 1);
```

<!-- tabs:end -->