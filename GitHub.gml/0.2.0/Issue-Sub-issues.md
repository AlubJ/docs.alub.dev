# Issue Sub-issues

## getIssueParent
`GitHub.getIssueParent(owner, repo, issueID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |

Get an issue's parent by its issueID.

[GitHub Documentation](https://docs.github.com/en/rest/issues/sub-issues#get-parent-issue).

#### **Example**

```gml
request = github.getIssueParent("AlubJ", "GitHub.gml", 48752187);
```

<!-- tabs:end -->

## removeSubIssue
`GitHub.removeSubIssue(owner, repo, issueID, subIssueID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `subIssueID` | `Real` | The ID of the sub-issue. |

Remove a sub-issue from an issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/sub-issues#remove-sub-issue).

#### **Example**

```gml
request = github.removeSubIssue("AlubJ", "GitHub.gml", 48752187, 548274);
```

<!-- tabs:end -->

## getSubIssues
`GitHub.getSubIssues(owner, repo, issueID, [perPage], [page]);`

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

Get an issue's parent by its issueID.

[GitHub Documentation](https://docs.github.com/en/rest/issues/sub-issues#list-sub-issues).

#### **Example**

```gml
request = github.getSubIssues("AlubJ", "GitHub.gml", 48752187, 10, 1);
```

<!-- tabs:end -->

## addSubIssue
`GitHub.addSubIssue(owner, repo, issueID, subIssueID, [replaceParent]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `subIssueID` | `Real` | The ID of the sub-issue. |
| `[replaceParent]` | `Bool` | Instructs the operation to replace the sub-issues current parent issue. |

Remove a sub-issue from an issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/sub-issues#add-sub-issue).

#### **Example**

```gml
request = github.addSubIssue("AlubJ", "GitHub.gml", 48752187, 1985815, false);
```

<!-- tabs:end -->

## reprioritizeSubIssue
`GitHub.reprioritizeSubIssue(owner, repo, issueID, subIssueID, [afterID], [beforeID]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The ID of the issue. |
| `subIssueID` | `Real` | The ID of the sub-issue. |
| `[afterID]` | `Bool` | The ID of the sub-issue to be prioritized after. |
| `[beforeID]` | `Bool` | The ID of the sub-issue to be prioritized before. |

Reprioritize a sub-issue.

[GitHub Documentation](https://docs.github.com/en/rest/issues/sub-issues#reprioritize-sub-issue).

#### **Example**

```gml
request = github.reprioritizeSubIssue("AlubJ", "GitHub.gml", 48752187, 1985815, 5698298, 918398);
```

<!-- tabs:end -->