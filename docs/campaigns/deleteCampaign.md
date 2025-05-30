---
name: Delete a campaign for an organization
example: octokit.rest.campaigns.deleteCampaign({ org, campaign_number })
route: DELETE /orgs/{org}/campaigns/{campaign_number}
scope: campaigns
type: API method
---

# Delete a campaign for an organization

Deletes a campaign in an organization.

The authenticated user must be an owner or security manager for the organization to use this endpoint.

OAuth app tokens and personal access tokens (classic) need the `security_events` scope to use this endpoint.

```js
octokit.rest.campaigns.deleteCampaign({
  org,
  campaign_number,
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
<tr><td>campaign_number</td><td>yes</td><td>

The campaign number.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/campaigns/campaigns#delete-a-campaign-for-an-organization).
