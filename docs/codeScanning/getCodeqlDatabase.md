---
name: Get a CodeQL database for a repository
example: octokit.rest.codeScanning.getCodeqlDatabase({ owner, repo, language })
route: GET /repos/{owner}/{repo}/code-scanning/codeql/databases/{language}
scope: codeScanning
type: API method
---

# Get a CodeQL database for a repository

Gets a CodeQL database for a language in a repository.

By default this endpoint returns JSON metadata about the CodeQL database. To
download the CodeQL database binary content, set the `Accept` header of the request
to [`application/zip`](https://docs.github.com/rest/using-the-rest-api/getting-started-with-the-rest-api#media-types), and make sure
your HTTP client is configured to follow redirects or use the `Location` header
to make a second request to get the redirect URL.

OAuth app tokens and personal access tokens (classic) need the `repo` scope to use this endpoint with private or public repositories, or the `public_repo` scope to use this endpoint with only public repositories.

```js
octokit.rest.codeScanning.getCodeqlDatabase({
  owner,
  repo,
  language,
});
```

## Parameters

<table>
  <thead>
    <tr>
      <th>name</th>
      <th>required</th>
      <th>description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>owner</td><td>yes</td><td>

The account owner of the repository. The name is not case sensitive.

</td></tr>
<tr><td>repo</td><td>yes</td><td>

The name of the repository without the `.git` extension. The name is not case sensitive.

</td></tr>
<tr><td>language</td><td>yes</td><td>

The language of the CodeQL database.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/code-scanning/code-scanning#get-a-codeql-database-for-a-repository).
