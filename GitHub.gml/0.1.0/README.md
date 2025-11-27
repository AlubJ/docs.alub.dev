GitHub.gml is a wrapper for the GitHub REST API written in GameMaker.

# Features
- Retrieve information about repository releases and issues.
- Create, update, edit and remove issues.
- Create, update, edit and remove releases.
- User authentication using OAuth.

# Updating
GitHub.gml uses semantic versioning. Major releases will introduce breaking changes and you'll have to rewrite some code. Minor releases will sometimes add something but never break compatibility.

?> Always make sure to read patch notes. Sometimes a minor breaking change can happen in minor versions, though very unlikely.

# GitHub API Details
[Current version] API implementation is for GitHub API version `2022-11-28`. Any updates to the GitHub API may break compatibility and it is recommended that you only use `2022-11-28`.

All API endpoints are based off of the default GitHub endpoints and very few edits are made. For more detailed documentation for what each endpoint is doing, please visit the [GitHub REST API documentation](https://docs.github.com/en/rest/). The endpoint API reference will link to each endpoint page.

# Installing
To install GitHub.gml, download the latest [.yymps](https://github.com/AlubJ/GitHub.gml/releases/latest). In GameMaker, go to `Tools >> Import local package` and select the downloaded .yymps. Make sure to import all assets and you're good to go.