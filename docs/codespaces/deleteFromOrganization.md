---
name: Delete a codespace from the organization
example: octokit.rest.codespaces.deleteFromOrganization({ org, username, codespace_name })
route: DELETE /orgs/{org}/members/{username}/codespaces/{codespace_name}
scope: codespaces
type: API method
---

# Delete a codespace from the organization

Deletes a user's codespace.

OAuth app tokens and personal access tokens (classic) need the `admin:org` scope to use this endpoint.

```js
octokit.rest.codespaces.deleteFromOrganization({
  org,
  username,
  codespace_name,
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
    <tr><td>org</td><td>yes</td><td>

The organization name. The name is not case sensitive.

</td></tr>
<tr><td>username</td><td>yes</td><td>

The handle for the GitHub user account.

</td></tr>
<tr><td>codespace_name</td><td>yes</td><td>

The name of the codespace.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/codespaces/organizations#delete-a-codespace-from-the-organization).
