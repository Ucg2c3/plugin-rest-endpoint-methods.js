---
name: Move a project card
example: octokit.rest.projects.moveCard({ card_id, position })
route: POST /projects/columns/cards/{card_id}/moves
scope: projects
type: API method
---

# Move a project card

**This method is deprecated.**

> [!WARNING] > **Closing down notice:** Projects (classic) is being deprecated in favor of the new Projects experience.
> See the [changelog](https://github.blog/changelog/2024-05-23-sunset-notice-projects-classic/) for more information.

```js
octokit.rest.projects.moveCard({
  card_id,
  position,
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
    <tr><td>card_id</td><td>yes</td><td>

The unique identifier of the card.

</td></tr>
<tr><td>position</td><td>yes</td><td>

The position of the card in a column. Can be one of: `top`, `bottom`, or `after:<card_id>` to place after the specified card.

</td></tr>
<tr><td>column_id</td><td>no</td><td>

The unique identifier of the column the card should be moved to

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/projects/cards#move-a-project-card).
