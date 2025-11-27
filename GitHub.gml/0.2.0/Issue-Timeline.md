# Issue Timeline

## getIssueTimelineEvents
`GitHub.getIssueTimelineEvents(owner, repo, issueID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get an issue's timeline events by its ID.

[GitHub Documentation](https://docs.github.com/en/rest/issues/timeline#list-timeline-events-for-an-issue).

#### **Example**

```gml
request = github.getIssueTimelineEvents("AlubJ", "GitHub.gml", 91589185, 10, 1);
```

<!-- tabs:end -->