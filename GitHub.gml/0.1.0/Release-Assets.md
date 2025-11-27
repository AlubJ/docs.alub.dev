# Release Assets

## getReleaseAsset
`GitHub.getReleaseAsset(owner, repo, assetID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `assetID` | `Real` | The asset ID of the repo. |

Get asset from a release.

[GitHub Documentation](https://docs.github.com/en/rest/releases/assets#get-a-release-asset).

#### **Example**

```gml
request = github.getReleaseAsset("AlubJ", "GitHub.gml", 205815);
```

<!-- tabs:end -->

## getReleaseAssets
`GitHub.getReleaseAssets(owner, repo, releaseID, [perPage], [page]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `releaseID` | `Real` | The release ID of the repo. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[page]` | `Real` | The page number of the results to fetch. |

Get asset from a release.

[GitHub Documentation](https://docs.github.com/en/rest/releases/assets#list-release-assets).

#### **Example**

```gml
request = github.getReleaseAssets("AlubJ", "GitHub.gml", 6988185, 10, 1);
```

<!-- tabs:end -->

## uploadReleaseAsset
`GitHub.uploadReleaseAsset(owner, repo, releaseID, buffer, contentType, targetFilename, [label]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `releaseID` | `Real` | The release ID of the repo. |
| `buffer` | `Id.Buffer` | The buffer to upload. |
| `contentType` | `String` | The content type of the release asset. |
| `targetFilename` | `String` | The target filename for the release asset. |
| `[label]` | `String` | The label for the release asset. |

Upload a release asset.

?> Buffers need to exist in memory until the request succeeds or fails. You can use a callback or errorback to delete the buffer.

[GitHub Documentation](https://docs.github.com/en/rest/releases/assets#upload-a-release-asset).

#### **Example**

```gml
// Load a buffer
var _buffer = buffer_load("myReleaseAsset.zip");

// Create an upload release asset request
request = github.uploadReleaseAsset("AlubJ", "GitHub.gml", 69881585, _buffer, "application/zip", "myApplicationRelease.zip", "Windows");
```

<!-- tabs:end -->

## updateReleaseAsset
`GitHub.updateReleaseAsset(owner, repo, assetID, filename, [label]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `assetID` | `Real` | The asset ID of the release. |
| `filename` | `String` | The updated filename. |
| `[label]` | `String` | The updated label. |

Update a release asset.

[GitHub Documentation](https://docs.github.com/en/rest/releases/assets#update-a-release-asset).

#### **Example**

```gml
request = github.updateReleaseAsset("AlubJ", "GitHub.gml", 205815, "myApplicationRelease", "Linux");
```

<!-- tabs:end -->

## deleteReleaseAsset
`GitHub.deleteReleaseAsset(owner, repo, assetID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `owner` | `String` | The owner of the repo. |
| `repo` | `String` | The repository name. |
| `assetID` | `Real` | The ID of the asset. |

Delete an existing release asset.

[GitHub Documentation](https://docs.github.com/en/rest/releases/assets#delete-a-release-asset).

#### **Example**

```gml
request = github.deleteReleaseAsset("AlubJ", "GitHub.gml", 205815);
```

<!-- tabs:end -->