# GitHub Constructors
GitHub.gml comes with helper constructors for certain aspects of the REST API, mainly dealing with more involved body based requests.

## GitHubIssue
`new GitHubIssue(title, [body], [assignee], [milestone], [labels], [assignees], [type], [state], [stateReason]);`

<!-- tabs:start -->

#### **Description**

`Returns` - GitHub Issue structure.

| Name | Type | Description |
| --- | --- | --- |
| `title` | `String` | The title of the issue. |
| `[body]` | `String` | The body or main content of the issue. |
| `[assignee]` | `String` | Login for the user this issue should be assigned to. |
| `[milestone]` | `Real` | Milestone number associated to this issue. |
| `[labels]` | `Array.String` | An array of labels to apply to the issue when created. |
| `[assignees]` | `Array.String` | An array of user to assign to the issue. |
| `[type]` | `String` | The name of the issue type to associate with this issue. |
| `[state]` | `String` | The state of the issue, either `open` or `closed` (only use when updating an issue). |
| `[stateReason]` | `String` | The state reason of the issue, either `completed`, `not_planned`, `duplicate`, `reopened` or `null` (only use when updating an issue). |

Creates a new GitHub Issue structure for use when creating or updating an issue. All properties can be accessed through the `.` or `[$]` accessor if you wish to reuse this struct.

[GitHub Documentation](https://docs.github.com/en/rest/issues/issues#create-an-issue).

#### **Example**

```gml
// Create issue struct
var _issue = new GitHubIssue("Uh oh... Something is broken!", "Game crashes :(", undefined, undefined, [ "bug", "crash" ], [ "AlubJ" ], undefined, "open", undefined);

// Create issue request
request = github.createIssue("AlubJ", "GitHub.gml", _issue);
```

<!-- tabs:end -->

## GitHubRelease
`new GitHubRelease(tagName, [targetCommitish], [name], [body], [draft], [prerelease], [discussionCategoryName], [generateReleaseNotes], [makeLatest]);`

<!-- tabs:start -->

#### **Description**

`Returns` - GitHub Release structure.

| Name | Type | Description |
| --- | --- | --- |
| `tagName` | `String` | The tag name for the release. |
| `[targetCommitish]` | `String` | Specifies the commitish value that determines where the Git tag is created from. |
| `[name]` | `String` | The name of the release. |
| `[body]` | `String` | The body or main content of the issue. |
| `[draft]` | `Bool` | Whether the release is a draft or not. |
| `[prerelease]` | `Bool` | Whether the release is a prerelease or not. |
| `[discussionCategoryName]` | `String` | The discussion category name for the release. |
| `[generateReleaseNotes]` | `Bool` | Whether to generate release notes based on the commit history for this release. |
| `[makeLatest]` | `Bool` | Whether to make this the latest release or not. |

Creates a new GitHub Release structure for use when creating or updating a release. All properties can be accessed through the `.` or `[$]` accessor if you wish to reuse this struct.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#create-a-release).

#### **Example**

```gml
// Create release struct
var _release = new GitHubRelease("v1.0.0", undefined, "v1.0 Release", "My release notes", false, false, undefined, true, true);

// Create release request
request = github.createRelease("AlubJ", "GitHub.gml", _release);
```

<!-- tabs:end -->

## GitHubGist
`new GitHubGist([description], [public]);`

<!-- tabs:start -->

#### **Description**

`Returns` - GitHub Release structure.

| Name | Type | Description |
| --- | --- | --- |
| `[description]` | `String` | The description of the gist. |
| `[public]` | `Bool` | Whether the gist is public or not. |

Creates a new GitHub Gist structure for use when creating or updating a gist. All properties can be accessed through the `.` or `[$]` accessor if you wish to reuse this struct. To add or remove files from this gist, call `addFile` and `removeFile`.

[GitHub Documentation](https://docs.github.com/en/rest/gists/gists#create-a-gist).

#### **Example**

```gml
// Create gist struct
var _gist = new GitHubGist("My Gist", true);
_gist.addFile("mycode.gml", "/// This is my code");

// Create gist request
request = github.createGist(_gist);
```

<!-- tabs:end -->