---
name: Delete an app token
example: octokit.rest.apps.deleteToken({ client_id, access_token })
route: DELETE /applications/{client_id}/token
scope: apps
type: API method
---

# Delete an app token

OAuth or GitHub application owners can revoke a single token for an OAuth application or a GitHub application with an OAuth authorization.

```js
octokit.rest.apps.deleteToken({
  client_id,
  access_token,
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
    <tr><td>client_id</td><td>yes</td><td>

The client ID of the GitHub app.

</td></tr>
<tr><td>access_token</td><td>yes</td><td>

The OAuth access token used to authenticate to the GitHub API.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/apps/oauth-applications#delete-an-app-token).
