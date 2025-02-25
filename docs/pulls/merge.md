---
name: Merge a pull request
example: octokit.rest.pulls.merge({ owner, repo, pull_number })
route: PUT /repos/{owner}/{repo}/pulls/{pull_number}/merge
scope: pulls
type: API method
---

# Merge a pull request

Merges a pull request into the base branch.
This endpoint triggers [notifications](https://docs.github.com/github/managing-subscriptions-and-notifications-on-github/about-notifications). Creating content too quickly using this endpoint may result in secondary rate limiting. For more information, see "[Rate limits for the API](https://docs.github.com/rest/using-the-rest-api/rate-limits-for-the-rest-api#about-secondary-rate-limits)" and "[Best practices for using the REST API](https://docs.github.com/rest/guides/best-practices-for-using-the-rest-api)."

```js
octokit.rest.pulls.merge({
  owner,
  repo,
  pull_number,
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
<tr><td>pull_number</td><td>yes</td><td>

The number that identifies the pull request.

</td></tr>
<tr><td>commit_title</td><td>no</td><td>

Title for the automatic commit message.

</td></tr>
<tr><td>commit_message</td><td>no</td><td>

Extra detail to append to automatic commit message.

</td></tr>
<tr><td>sha</td><td>no</td><td>

SHA that pull request head must match to allow merge.

</td></tr>
<tr><td>merge_method</td><td>no</td><td>

The merge method to use.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/pulls/pulls#merge-a-pull-request).
