---
name: Delete an app authorization
example: octokit.rest.apps.deleteAuthorization({ client_id, access_token })
route: DELETE /applications/{client_id}/grant
scope: apps
type: API method
---

# Delete an app authorization

OAuth and GitHub application owners can revoke a grant for their application and a specific user. You must provide a valid OAuth `access_token` as an input parameter and the grant for the token's owner will be deleted.
Deleting an application's grant will also delete all OAuth tokens associated with the application for the user. Once deleted, the application will have no access to the user's account and will no longer be listed on [the application authorizations settings screen within GitHub](https://github.com/settings/applications#authorized).

```js
octokit.rest.apps.deleteAuthorization({
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

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/apps/oauth-applications#delete-an-app-authorization).
