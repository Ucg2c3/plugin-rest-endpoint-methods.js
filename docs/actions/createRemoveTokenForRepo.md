---
name: Create a remove token for a repository
example: octokit.rest.actions.createRemoveTokenForRepo({ owner, repo })
route: POST /repos/{owner}/{repo}/actions/runners/remove-token
scope: actions
type: API method
---

# Create a remove token for a repository

Returns a token that you can pass to the `config` script to remove a self-hosted runner from an repository. The token expires after one hour.

For example, you can replace `TOKEN` in the following example with the registration token provided by this endpoint to remove your self-hosted runner from an organization:

```
./config.sh remove --token TOKEN
```

Authenticated users must have admin access to the repository to use this endpoint.

OAuth tokens and personal access tokens (classic) need the `repo` scope to use this endpoint.

```js
octokit.rest.actions.createRemoveTokenForRepo({
  owner,
  repo,
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
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/actions/self-hosted-runners#create-a-remove-token-for-a-repository).
