# Issues

## getIssuesAssignedToMe
`GitHub.getIssuesAssignedToMe([filter], [state], [labels], [sort], [direction], [since], [collab], [orgs], [owned], [pulls], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `[filter]` | `String` | Filter by "assigned", "created", "mentioned", "subscribed", "repos" or "all". |
| `[state]` | `String` | Issue state filter by "open", "closed" or "all". |
| `[labels]` | `String` | Issue labels separated by commas ("bug,ui,@high"). |
| `[sort]` | `String` | Sort by "created" or "updated". |
| `[direction]` | `String` | Direction to sort by, "asc" or "desc". |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[collab]` | `Bool` | No description provided. |
| `[orgs]` | `Bool` | No description provided. |
| `[owned]` | `Bool` | No description provided. |
| `[pulls]` | `Bool` | No description provided. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get all the issues assigned to the authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#list-issues-assigned-to-the-authenticated-user).

#### **Example**

```gml
request = github.getIssuesAssignedToMe("assigned", "open", "bug", "created", "desc", undefined, false, false, false, false, 10, 1);
```

<!-- tabs:end -->

## getOrgIssuesAssignedToMe
`GitHub.getOrgIssuesAssignedToMe(org, [filter], [state], [labels], [sort], [direction], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `org` | `String` | The organization. |
| `[filter]` | `String` | Filter by "assgined", "created", "mentioned", "subscribed", "repos" or "all". |
| `[state]` | `String` | Issue state filter by "open", "closed" or "all". |
| `[labels]` | `String` | Issue labels separated by commas ("bug,ui,@high"). |
| `[sort]` | `String` | Sort by "created" or "updated". |
| `[direction]` | `String` | Direction to sort by, "asc" or "desc". |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get an organizations issues assigned to the authenticated user.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#list-organization-issues-assigned-to-the-authenticated-user).

#### **Example**

```gml
request = github.getOrgIssuesAssignedToMe("My Org", "assigned", "open", "bug", "created", "desc", undefined, 10, 1);
```

<!-- tabs:end -->

## getIssues
`GitHub.getIssues(owner, repo, [milestone], [state], [assignee], [type], [creator], [mentioned], [labels], [sort], [direction], [since], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[milestone]` | `Real` | Pass an integer to refer to a specific milestone, pass "*" to refer to all milestones or pass "none" to omit issues without milestones. |
| `[state]` | `String` | Issue state filter by "open", "closed" or "all". |
| `[assignee]` | `String` | Filter by the user assigned. |
| `[type]` | `String` | Filter by the issue type. |
| `[creator]` | `String` | Filter by the user who created the issue. |
| `[mentioned]` | `String` | Filter by a user who was mentioned in the issue. |
| `[labels]` | `String` | Issue labels separated by commas ("bug,ui,@high"). |
| `[sort]` | `String` | Sort by "created" or "updated". |
| `[direction]` | `String` | Direction to sort by, "asc" or "desc". |
| `[since]` | `String` | Only show results that were updated after the given time. (`YYYY-MM-DDTHH:MM:SSZ`). |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get issues from a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#list-repository-issues).

#### **Example**

```gml
request = github.getIssues("AlubJ", "GitHub.gml", "*", "open", undefined, undefined, "AlubJ", undefined, undefined, "bug", "created", "asc", undefined, 10, 1);
```

<!-- tabs:end -->

## createIssue
`GitHub.createIssue(owner, repo, issue);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issue` | `Struct.GitHubIssue` | The issue struct. |

Create a new issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#create-an-issue).

#### **Example**

```gml
// Create a new issue
var _issue = new GitHubIssue("My Issue", "Something is not working :(", "AlubJ", undefined, [ "bug", "crash" ], undefined);

// Create the request
request = github.createIssue("AlubJ", "GitHub.gml", _issue);
```

<!-- tabs:end -->

## getIssue
`GitHub.getIssue(owner, repo, issueID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |

Get an issue by its issueID.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#get-an-issue).

#### **Example**

```gml
request = github.getIssue("AlubJ", "GitHub.gml", 68982985);
```

<!-- tabs:end -->

## updateIssue
`GitHub.updateIssue(owner, repo, issueID, issue);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `issue` | `Struct.GitHubIssue` | The issue struct. |

Update an existing issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#update-an-issue).

#### **Example**

```gml
// Update issue
_issue.state = "closed";
_issue.stateReason = "not_planned";

// Create the request
request = github.updateIssue("AlubJ", "GitHub.gml", _issue);
```

<!-- tabs:end -->

## lockIssue
`GitHub.lockIssue(owner, repo, issueID, lockReason);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `lockReason` | `String` | The reason for locking, can be "off-topic", "too heated", "resolved" or "spam" |

Lock an existing issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#lock-an-issue).

#### **Example**

```gml
request = github.lockIssue("AlubJ", "GitHub.gml", 68982985, "off-topic");
```

<!-- tabs:end -->

## unlockIssue
`GitHub.unlockIssue(owner, repo, issueID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |

Unlock a locked issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#unlock-an-issue).

#### **Example**

```gml
request = github.unlockIssue("AlubJ", "GitHub.gml", 68982985);
```

<!-- tabs:end -->