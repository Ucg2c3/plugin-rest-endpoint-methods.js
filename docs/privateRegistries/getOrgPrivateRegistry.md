---
name: Get a private registry for an organization
example: octokit.rest.privateRegistries.getOrgPrivateRegistry({ org, secret_name })
route: GET /orgs/{org}/private-registries/{secret_name}
scope: privateRegistries
type: API method
---

# Get a private registry for an organization

Get the configuration of a single private registry defined for an organization, omitting its encrypted value.

OAuth app tokens and personal access tokens (classic) need the `admin:org` scope to use this endpoint.

```js
octokit.rest.privateRegistries.getOrgPrivateRegistry({
  org,
  secret_name,
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
<tr><td>secret_name</td><td>yes</td><td>

The name of the secret.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/private-registries/organization-configurations#get-a-private-registry-for-an-organization).
