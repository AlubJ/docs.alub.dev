# Issue Comments

## getRepoIssueComments
`GitHub.getRepoIssueComments(owner, repo, [sort], [direction], [since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[sort]` | `String` | Sort by "created" or "updated". |
| `[direction]` | `String` | Direction to sort by, "asc" or "desc". |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get all issue comments in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#list-issue-comments-for-a-repository).

#### **Example**

```gml
request = github.getRepoIssueComments("AlubJ", "GitHub.gml", "created", "asc", undefined, 10, 1);
```

<!-- tabs:end -->

## getIssueComment
`GitHub.getIssueComment(owner, repo, commentID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `commentID` | `Real` | The comment ID. |

Get an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#get-an-issue-comment).

#### **Example**

```gml
request = github.getIssueComment("AlubJ", "GitHub.gml", 8578782);
```

<!-- tabs:end -->

## updateIssueComment
`GitHub.updateIssueComment(owner, repo, commentID, body);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `commentID` | `Real` | The comment ID. |
| `body` | `String` | The body of the comment. |

Update an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#update-an-issue-comment).

#### **Example**

```gml
request = github.updateIssueComment("AlubJ", "GitHub.gml", 8578782, "Updated comment!");
```

<!-- tabs:end -->

## deleteIssueComment
`GitHub.deleteIssueComment(owner, repo, commentID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `commentID` | `Real` | The comment ID. |

Delete an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#delete-an-issue-comment).

#### **Example**

```gml
request = github.deleteIssueComment("AlubJ", "GitHub.gml", 8578782);
```

<!-- tabs:end -->

## getIssueComments
`GitHub.getIssueComments(owner, repo, issueID, [since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The repository name. |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get an issues comments in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#list-issue-comments).

#### **Example**

```gml
request = github.getIssueComments("AlubJ", "GitHub.gml", 1769549, undefined, 10, 1);
```

<!-- tabs:end -->

## createIssueComment
`GitHub.createIssueComment(owner, repo, issueID, _body);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The repository name. |
| `body` | `String` | The body of the issue comment. |

Create an issue comment in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/comments#create-an-issue-comment).

#### **Example**

```gml
request = github.deleteIssueComment("AlubJ", "GitHub.gml", 1769549, "This is a new comment!");
```

<!-- tabs:end -->