---
name: Cancel a workflow run
example: octokit.rest.actions.cancelWorkflowRun({ owner, repo, run_id })
route: POST /repos/{owner}/{repo}/actions/runs/{run_id}/cancel
scope: actions
type: API method
---

# Cancel a workflow run

Cancels a workflow run using its `id`.

OAuth tokens and personal access tokens (classic) need the `repo` scope to use this endpoint.

```js
octokit.rest.actions.cancelWorkflowRun({
  owner,
  repo,
  run_id,
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
<tr><td>run_id</td><td>yes</td><td>

The unique identifier of the workflow run.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/actions/workflow-runs#cancel-a-workflow-run).
