---
name: Download a repository archive (tar)
example: octokit.rest.repos.downloadTarballArchive({ owner, repo, ref })
route: GET /repos/{owner}/{repo}/tarball/{ref}
scope: repos
type: API method
---

# Download a repository archive (tar)

Gets a redirect URL to download a tar archive for a repository. If you omit `:ref`, the repository’s default branch (usually
`main`) will be used. Please make sure your HTTP framework is configured to follow redirects or you will need to use
the `Location` header to make a second `GET` request.

> [!NOTE]
> For private repositories, these links are temporary and expire after five minutes.

```js
octokit.rest.repos.downloadTarballArchive({
  owner,
  repo,
  ref,
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
<tr><td>ref</td><td>yes</td><td>

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/repos/contents#download-a-repository-archive-tar).
