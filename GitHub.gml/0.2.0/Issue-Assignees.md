# Issue Assignees

## getAssignees
`GitHub.getAssignees(owner, repo, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get assignees / contributors in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/assignees#list-assignees).

#### **Example**

```gml
request = github.getAssignees("AlubJ", "GitHub.gml", 10, 1);
```

<!-- tabs:end -->

## userAssignable
`GitHub.userAssignable(owner, repo, assignee);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `assignee` | `String` | The assignee name. |

Get assignees / contributors in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/assignees#check-if-a-user-can-be-assigned).

#### **Example**

```gml
request = github.userAssignable("AlubJ", "GitHub.gml", "User");
```

<!-- tabs:end -->

## addAssigneesToIssue
`GitHub.addAssigneesToIssue(owner, repo, issueID, assignees);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID / number. |
| `assignees` | `Array.String` | List of assignees. |

Add assignees / contributors in a repository to an issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/assignees#add-assignees-to-an-issue).

#### **Example**

```gml
request = github.addAssigneesToIssue("AlubJ", "GitHub.gml", 958158, [ "User1", "User2" ]);
```

<!-- tabs:end -->

## removeAssigneesFromIssue
`GitHub.removeAssigneesFromIssue(owner, repo, issueID, assignees);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID / number. |
| `assignees` | `Array.String` | List of assignees. |

Remove assignees / contributors in a repository from an issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/assignees#remove-assignees-from-an-issue).

#### **Example**

```gml
request = github.removeAssigneesFromIssue("AlubJ", "GitHub.gml", 958158, [ "User1", "User2" ]);
```

<!-- tabs:end -->

## userAssignableToIssue
`GitHub.userAssignableToIssue(owner, repo, issueID, assignee);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID / number. |
| `assignee` | `String` | The assignee name. |

Get assignees / contributors in a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/assignees#check-if-a-user-can-be-assigned-to-a-issue).

#### **Example**

```gml
request = github.userAssignableToIssue("AlubJ", "GitHub.gml", 958158, "User1");
```

<!-- tabs:end -->