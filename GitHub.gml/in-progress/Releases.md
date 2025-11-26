# Releases

## getLatestRelease
`GitHub.getLatestRelease(owner, repo);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |

Creates a new GitHub request to get the latest release from a give repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#get-the-latest-release).

#### **Example**

Create:
```gml
// Create request
request = github.getLatestRelease("AlubJ", "GitHub.gml");
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## getReleases
`GitHub.getReleases(owner, repo, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Creates a new GitHub request to get a list of releases from a give repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#list-releases).

#### **Example**

Create:
```gml
// Create request
request = github.getReleases("AlubJ", "GitHub.gml", 20, 1);
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## getReleaseByTag
`GitHub.getReleaseByTag(owner, repo, tagName);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `tagName` | `String` | The tag name of the release. |

Creates a new GitHub request to get a release by a given tag name from a give repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#get-a-release-by-tag-name).

#### **Example**

Create:
```gml
// Create request
request = github.getReleaseByTag("AlubJ", "GitHub.gml", "v1.0.0");
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## getRelease
`GitHub.getRelease(owner, repo, releaseID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `releaseID` | `Real` | The ID of the release. |

Creates a new GitHub request to get a release by a given release ID from a give repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#get-a-release).

#### **Example**

Create:
```gml
// Create request
request = github.getRelease("AlubJ", "GitHub.gml", 25881904);
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## createRelease
`GitHub.createRelease(owner, repo, release);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `release` | `Struct.GitHubRelease` | The release struct. |

Creates a new GitHub request to create a new release to a given repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#create-a-release).

#### **Example**

Create:
```gml
// Create release struct
var _release = new GitHubRelease("v1.0.0", undefined, "v1.0 Release", "My release notes", false, false, undefined, true, true);

// Create release request
request = github.createRelease("AlubJ", "GitHub.gml", _release);
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## updateRelease
`GitHub.updateRelease(owner, repo, releaseID, release);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `releaseID` | `Real` | The ID of the release. |
| `release` | `Struct.GitHubRelease` | The release struct. |

Creates a new GitHub request to update an existing release in a given repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#update-a-release).

#### **Example**

Create:
```gml
// Create update release struct
var _release = new GitHubRelease("v1.0.0", undefined, "v1.0 Release", "My release notes", false, false, undefined, true, true);

// Create release request
request = github.updateRelease("AlubJ", "GitHub.gml", 2481593, _release);
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->

## deleteRelease
`GitHub.deleteRelease(owner, repo, releaseID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `releaseID` | `Real` | The ID of the release. |

Creates a new GitHub request to delete an existing release in a given repository.

[GitHub Documentation](https://docs.github.com/en/rest/releases/releases#delete-a-release).

#### **Example**

Create:
```gml
// Delete release request
request = github.deleteRelease("AlubJ", "GitHub.gml", 2481593);
```

Step:
```gml
// Check request
if (request.httpStatus == 200)
{
    show_message(json_stringify(request.result));
}
```

<!-- tabs:end -->