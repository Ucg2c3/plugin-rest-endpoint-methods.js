---
name: Get a discussion comment
example: octokit.rest.teams.getDiscussionCommentInOrg({ org, team_slug, discussion_number, comment_number })
route: GET /orgs/{org}/teams/{team_slug}/discussions/{discussion_number}/comments/{comment_number}
scope: teams
type: API method
---

# Get a discussion comment

Get a specific comment on a team discussion.

> [!NOTE]
> You can also specify a team by `org_id` and `team_id` using the route `GET /organizations/{org_id}/team/{team_id}/discussions/{discussion_number}/comments/{comment_number}`.

OAuth app tokens and personal access tokens (classic) need the `read:discussion` scope to use this endpoint.

```js
octokit.rest.teams.getDiscussionCommentInOrg({
  org,
  team_slug,
  discussion_number,
  comment_number,
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
<tr><td>team_slug</td><td>yes</td><td>

The slug of the team name.

</td></tr>
<tr><td>discussion_number</td><td>yes</td><td>

The number that identifies the discussion.

</td></tr>
<tr><td>comment_number</td><td>yes</td><td>

The number that identifies the comment.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/teams/discussion-comments#get-a-discussion-comment).
