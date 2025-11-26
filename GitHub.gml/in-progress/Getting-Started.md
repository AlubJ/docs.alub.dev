# Getting Started

There's a couple things that you need to do before the GitHub API is ready to use.

## Set-up GitHub
To use the API, you'll need to construct a new `GitHub`, ideally as a global variable. GitHub.gml intends to support multiple instances of the API in use, this is great if you're working with multiple repositories.

```gml
global.github = new GitHub("your-auth-token");
```

?> An authentication token is not strictly necessary to use the GitHub API however you may encounter API rate limits or certain endpoints returning `403`.

!> GitHub.gml DOES NOT attempt to hide your authentication token and it is not recommended that you ship GitHub.gml with your final game.

## Setting Your User-Agent
GitHub requires a valid user agent to be set when making requests to the API. The user agent can be anything, however it has to be set. By default, the user agent is set to `Alub`. To change the default, open the `__GitHubConfig` script and edit the `GITHUB_GML_USER_AGENT` macro to a new user agent.

## Testing GitHub.gml
Here is some sample code you can use to test GitHub.gml. This will make a request to get the latest release from GitHib.gml, once the HTTP status of the request becomes `200`, it will show a message with the result of the request.

Create:
```gml
// Create GitHub instance
github = new GitHub();

// Create a request to get the latest release of GitHub.gml
request = github.getLatestRelease("AlubJ", "GitHub.gml");
requestComplete = false;
```

Step:
```gml
// Check request returns 200
if (request.httpStatus == 200 && !requestComplete)
{
    show_message(request.result);
    requestComplete = true;
}
```