# Issue Labels

## getIssueLabels
`GitHub.getIssueLabels(owner, repo, issueID, [perPage], [page]);`

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

Get an issue's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#list-labels-for-an-issue).

#### **Example**

```gml
request = github.getIssueLabels("AlubJ", "GitHub.gml", 5917615, 10, 1);
```

<!-- tabs:end -->

## addIssueLabels
`GitHub.addIssueLabels(owner, repo, issueID, labels);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID. |
| `labels` | `Array.String` | Array of labels to add to the issue. |

Get an issue's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#add-labels-to-an-issue).

#### **Example**

```gml
request = github.addIssueLabels("AlubJ", "GitHub.gml", 5917615, [ "bug", "crash" ]);
```

<!-- tabs:end -->

## setIssueLabels
`GitHub.setIssueLabels(owner, repo, issueID, labels);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID. |
| `labels` | `Array.String` | Array of labels to set to the issue. |

Set an issue's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#set-labels-for-an-issue).

#### **Example**

```gml
request = github.setIssueLabels("AlubJ", "GitHub.gml", 5917615, [ "bug", "crash" ]);
```

<!-- tabs:end -->

## removeAllIssueLabels
`GitHub.removeAllIssueLabels(owner, repo, issueID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID. |

Set an issue's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#remove-all-labels-from-an-issue).

#### **Example**

```gml
request = github.removeAllIssueLabels("AlubJ", "GitHub.gml", 5917615);
```

<!-- tabs:end -->

## removeIssueLabel
`GitHub.removeIssueLabel(owner, repo, issueID, labelName);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `issueID` | `Real` | The issue ID. |
| `labelName` | `String` | The label name to remove. |

Set an issue's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#remove-a-label-from-an-issue).

#### **Example**

```gml
request = github.removeAllIssueLabels("AlubJ", "GitHub.gml", 5917615, "bug");
```

<!-- tabs:end -->

## getLabels
`GitHub.getLabels(owner, repo, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get a repository's labels.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#list-labels-for-a-repository).

#### **Example**

```gml
request = github.getLabels("AlubJ", "GitHub.gml", 10, 1);
```

<!-- tabs:end -->

## createLabel
`GitHub.createLabel(owner, repo, name, [color], [description]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `name` | `String` | The name of the new label. |
| `[color]` | `Constant.Color` | The color of the new label. |
| `[description]` | `String` | The description of the new label. |

Create a new label for a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#create-a-label).

#### **Example**

```gml
request = github.createLabel("AlubJ", "GitHub.gml", "documentation request", c_maroon, "A new documentation page or feature.");
```

<!-- tabs:end -->

## getLabel
`GitHub.getLabel(owner, repo, labelName);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `labelName` | `String` | The label name to remove. |

Get a repository label by name.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#get-a-label).

#### **Example**

```gml
request = github.getLabel("AlubJ", "GitHub.gml", "documentation request");
```

<!-- tabs:end -->

## updateLabel
`GitHub.updateLabel(owner, repo, name, [newName], [color], [description]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `name` | `String` | The name of the label. |
| `[newName]` | `String` | The new name of the label. |
| `[color]` | `Constant.Color` | The new color of the label. |
| `[description]` | `String` | The new description of the label. |

Update an existing label for a repository.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#update-a-label).

#### **Example**

```gml
request = github.updateLabel("AlubJ", "GitHub.gml", "documentation request", "Documentation Request", c_red, "A new documentation page or feature.");
```

<!-- tabs:end -->

## deleteLabel
`GitHub.deleteLabel(owner, repo, labelName);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `labelName` | `String` | The label name to remove. |

Delete a repository label by name.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#delete-a-label).

#### **Example**

```gml
request = github.deleteLabel("AlubJ", "GitHub.gml", "documentation request");
```

<!-- tabs:end -->

## getIssueMilestoneLabels
`GitHub.getIssueMilestoneLabels(owner, repo, milestoneID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `milestoneID` | `Real` | The milestone number. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get an issues labels in a milestone.

[GitHub Documentation](https://docs.github.com/en/rest/issues/labels#list-labels-for-issues-in-a-milestone).

#### **Example**

```gml
request = github.getIssueMilestoneLabels("AlubJ", "GitHub.gml", 1, 10, 1);
```

<!-- tabs:end -->