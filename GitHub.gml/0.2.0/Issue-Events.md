# Issue Events

## getRepoIssueEvents
`GitHub.getRepoIssueEvents(owner, repo, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a repositories issue events.

[GitHub Documentation](https://docs.github.com/en/rest/issues/events#list-issue-events-for-a-repository).

#### **Example**

```gml
request = github.getRepoIssueEvents("AlubJ", "GitHub.gml", 10, 1);
```

<!-- tabs:end -->

## getIssueEvent
`GitHub.getIssueEvent(owner, repo, eventID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `eventID` | `Real` | The event ID. |

Get a repository issue event.

[GitHub Documentation](https://docs.github.com/en/rest/issues/events#get-an-issue-event).

#### **Example**

```gml
request = github.getIssueEvent("AlubJ", "GitHub.gml", 5981834);
```

<!-- tabs:end -->

## getIssueEvents
`GitHub.getIssueEvents(owner, repo, issueID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get an issues events.

[GitHub Documentation](https://docs.github.com/en/rest/issues/events#list-issue-events).

#### **Example**

```gml
request = github.getIssueEvents("AlubJ", "GitHub.gml", 19684491);
```

<!-- tabs:end -->