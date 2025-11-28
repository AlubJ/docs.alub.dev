# Configuration

There is a couple of configurable options that GitHub.gml provides. You can find them in `(Config) > __GitHubConfig`.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| `GITHUB_GML_API_VERSION` | `String` | `"2022-11-28"` | The GitHub API has numerous versions to work with. GitHub.gml is designed to work with the latest version at the time of writing (2022-11-28). |
| `GITHUB_GML_USER_AGENT` | `String` | `"GitHub.gml/v0.2.0"` | The GitHub API requires a user agent to be set when making requests to the API endpoints. |
| `GITHUB_GML_OAUTH_MAX_POLLS` | `Real` | `20` | The maximum amount of times that GitHubOAuth can poll the authentication request before it times out. |
| `GITHUB_GML_OAUTH_MAX_POLL_INTERVAL` | `Real` | `60` | The maximum amount of time in seconds that GitHubOAuth can poll the authentication request, the minimum should be whatever the OAuth request sends back. |
| `GITHUB_GML_LOCALHOST_PORT` | `Real` | `52499` | Port to connect on as part of the `.requestAuthenticationViaWebPage()` flow. This must match the callback URL entered whe creating your GitHub app. e.g. Setting `GITHUB_GML_LOCALHOST_PORT` to `52499` means that you should use `http://localhost:52499/` for the callback URL. |
| `GITHUB_GML_SERVER_SHUTDOWN_TIME` | `Real` | `1` | The time in seconds it takes to shutdown the web-server for web-flow authentication. This is here to allow enough time for the HTML to be served to the |