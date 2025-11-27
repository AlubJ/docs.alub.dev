# Issue Milestones

## getMilestones
`GitHub.getMilestones(owner, repo, [state], [sort], [direction], [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[state]` | `String` | Issue state filter by "open", "closed" or "all". |
| `[sort]` | `String` | Sort by "created" or "updated". |
| `[direction]` | `String` | Direction to sort by, "asc" or "desc". |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a repository's milestones.

[GitHub Documentation](https://docs.github.com/en/rest/issues/milestones#list-milestonese).

#### **Example**

```gml
request = github.getMilestones("AlubJ", "GitHub.gml", "open", "created", "asc", 10, 1);
```

<!-- tabs:end -->

## createMilestone
`GitHub.createMilestone(owner, repo, title, [state], [description], [dueOn]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `title` | `String` | The title of the new milestone. |
| `[state]` | `String` | State of milestone "open" or "closed". |
| `[description]` | `String` | Description of the milestone. |
| `[dueOn]` | `String` | The due on time. (`YYYY-MM-DDTHH:MM:SSZ`). |

Create a new milestone for a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/milestones#create-a-milestone).

#### **Example**

```gml
request = github.createMilestone("AlubJ", "GitHub.gml", "Completed Feature", "closed", "The feature is completed!", undefined);
```

<!-- tabs:end -->

## getMilestone
`GitHub.getMilestone(owner, repo, milestoneID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `milestoneID` | `Real` | The ID of the milestone. |

Get a repository milestone.

[GitHub Documentation](https://docs.github.com/en/rest/issues/milestones#get-a-milestone).

#### **Example**

```gml
request = github.getMilestone("AlubJ", "GitHub.gml", 1);
```

<!-- tabs:end -->

## updateMilestone
`GitHub.updateMilestone(owner, repo, milestoneID, [title], [state], [description], [dueOn]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `milestoneID` | `Real` | The ID of the milestone. |
| `[title]` | `String` | The new title of the milestone. |
| `[state]` | `String` | State of milestone "open" or "closed". |
| `[description]` | `String` | Description of the milestone. |
| `[dueOn]` | `String` | The due on time. (`YYYY-MM-DDTHH:MM:SSZ`). |

Create a new milestone for a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/milestones#update-a-milestone).

#### **Example**

```gml
request = github.updateMilestone("AlubJ", "GitHub.gml", 1, "New milestone title", "open", "This is a new description", "2025-12-16T00:00:00Z");
```

<!-- tabs:end -->

## deleteMilestone
`GitHub.deleteMilestone(owner, repo, milestoneID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `milestoneID` | `Real` | The ID of the milestone. |

Delete a milestone from a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/milestones#delete-a-milestone).

#### **Example**

```gml
request = github.deleteMilestone("AlubJ", "GitHub.gml", 1);
```

<!-- tabs:end -->