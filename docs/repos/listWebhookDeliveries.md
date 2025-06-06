---
name: List deliveries for a repository webhook
example: octokit.rest.repos.listWebhookDeliveries({ owner, repo, hook_id })
route: GET /repos/{owner}/{repo}/hooks/{hook_id}/deliveries
scope: repos
type: API method
---

# List deliveries for a repository webhook

Returns a list of webhook deliveries for a webhook configured in a repository.

```js
octokit.rest.repos.listWebhookDeliveries({
  owner,
  repo,
  hook_id,
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
<tr><td>hook_id</td><td>yes</td><td>

The unique identifier of the hook. You can find this value in the `X-GitHub-Hook-ID` header of a webhook delivery.

</td></tr>
<tr><td>per_page</td><td>no</td><td>

The number of results per page (max 100). For more information, see "[Using pagination in the REST API](https://docs.github.com/rest/using-the-rest-api/using-pagination-in-the-rest-api)."

</td></tr>
<tr><td>cursor</td><td>no</td><td>

Used for pagination: the starting delivery from which the page of deliveries is fetched. Refer to the `link` header for the next and previous page cursors.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/repos/webhooks#list-deliveries-for-a-repository-webhook).
