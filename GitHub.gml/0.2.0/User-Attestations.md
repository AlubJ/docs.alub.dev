# User Attestations

## getAttestationsBySubjectDigests
`GitHub.getAttestationsBySubjectDigests(username, subjectDigests, [predicateType], [perPage], [before], [after]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The handle for the GitHub user account. |
| `subjectDigests` | `Array.String` | List of subject digests to fetch attestations for. |
| `[predicateType]` | `String` | Filter for fetching attestations with a given predicate type. This option accepts "provenance", "sbom", "release", or "freeform" text for custom predicate types. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[before]` | `Real` | A cursor, as given in the Link header. |
| `[after]` | `Real` | A cursor, as given in the Link header. |

Get a list of attestations by bulk subject digests.

[GitHub Documentation](https://docs.github.com/en/rest/users/attestations#list-attestations-by-bulk-subject-digests).

#### **Example**

```gml
No example provided.
```

<!-- tabs:end -->

## deleteAttestationBySubjectDigest
`GitHub.deleteAttestationBySubjectDigest(username, subjectDigest);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The handle for the GitHub user account. |
| `subjectDigest` | `String` | Subject digests to delete attestations for. |

Delete an artifact attestation by subject digest.

[GitHub Documentation](https://docs.github.com/en/rest/users/attestations#delete-attestations-by-subject-digest).

#### **Example**

```gml
No example provided.
```

<!-- tabs:end -->

## deleteAttestationByID
`GitHub.deleteAttestationByID(username, attestationID);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The handle for the GitHub user account. |
| `attestationID` | `Real` | Attestation ID to delete attestations for. |

Delete an artifact attestation by subject digest.

[GitHub Documentation](https://docs.github.com/en/rest/users/attestations#delete-attestations-by-id).

#### **Example**

```gml
No example provided.
```

<!-- tabs:end -->

## getAttestations
`GitHub.getAttestations(username, subjectDigest, [perPage], [before], [after], [predicateType]);`

<!-- tabs:start -->

#### **Description**

`Returns` - [GitHub Request](Requests.md#github-request).

| Name | Type | Description |
| --- | --- | --- |
| `username` | `String` | The handle for the GitHub user account. |
| `subjectDigest` | `String` | Subject digests to delete attestations for. |
| `[perPage]` | `Real` | The number of results per page (max 100). |
| `[before]` | `Real` | A cursor, as given in the Link header. |
| `[after]` | `Real` | A cursor, as given in the Link header. |
| `[predicateType]` | `String` | Filter for fetching attestations with a given predicate type. This option accepts "provenance", "sbom", "release", or "freeform" text for custom predicate types. |

List a collection of artifact attestations with a given subject digest that are associated with repositories owned by a user.

[GitHub Documentation](https://docs.github.com/en/rest/users/attestations#list-attestations).

#### **Example**

```gml
No example provided.
```

<!-- tabs:end -->