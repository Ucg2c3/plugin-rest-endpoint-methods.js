---
name: Get all organization repository rulesets
example: octokit.rest.repos.getOrgRulesets({ org })
route: GET /orgs/{org}/rulesets
scope: repos
type: API method
---

# Get all organization repository rulesets

Get all the repository rulesets for an organization.

```js
octokit.rest.repos.getOrgRulesets({
  org,
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
<tr><td>per_page</td><td>no</td><td>

The number of results per page (max 100). For more information, see "[Using pagination in the REST API](https://docs.github.com/rest/using-the-rest-api/using-pagination-in-the-rest-api)."

</td></tr>
<tr><td>page</td><td>no</td><td>

The page number of the results to fetch. For more information, see "[Using pagination in the REST API](https://docs.github.com/rest/using-the-rest-api/using-pagination-in-the-rest-api)."

</td></tr>
<tr><td>targets</td><td>no</td><td>

A comma-separated list of rule targets to filter by.
If provided, only rulesets that apply to the specified targets will be returned.
For example, `branch,tag,push`.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/orgs/rules#get-all-organization-repository-rulesets).
