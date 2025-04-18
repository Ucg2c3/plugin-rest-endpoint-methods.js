---
name: Get a summary of Copilot usage for a team
example: octokit.rest.copilot.usageMetricsForTeam({ org, team_slug })
route: GET /orgs/{org}/team/{team_slug}/copilot/usage
scope: copilot
type: API method
---

# Get a summary of Copilot usage for a team

> [!NOTE]
> This endpoint is closing down. It will be accessible throughout February 2025, but will not return any new data after February 1st.

You can use this endpoint to see a daily breakdown of aggregated usage metrics for Copilot completions and Copilot Chat in the IDE
for users within a team, with a further breakdown of suggestions, acceptances, and number of active users by editor and language for each day.
See the response schema tab for detailed metrics definitions.

The response contains metrics for up to 28 days prior. Usage metrics are processed once per day for the previous day,
and the response will only include data up until yesterday. In order for an end user to be counted towards these metrics,
they must have telemetry enabled in their IDE.

> [!NOTE]
> This endpoint will only return results for a given day if the team had five or more members with active Copilot licenses, as evaluated at the end of that day.

Organization owners for the organization that contains this team, and owners and billing managers of the parent enterprise can view Copilot usage metrics for a team.

OAuth app tokens and personal access tokens (classic) need either the `manage_billing:copilot`, `read:org`, or `read:enterprise` scopes to use this endpoint.

```js
octokit.rest.copilot.usageMetricsForTeam({
  org,
  team_slug,
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
<tr><td>since</td><td>no</td><td>

Show usage metrics since this date. This is a timestamp in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format (`YYYY-MM-DDTHH:MM:SSZ`). Maximum value is 28 days ago.

</td></tr>
<tr><td>until</td><td>no</td><td>

Show usage metrics until this date. This is a timestamp in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format (`YYYY-MM-DDTHH:MM:SSZ`) and should not preceed the `since` date if it is passed.

</td></tr>
<tr><td>page</td><td>no</td><td>

The page number of the results to fetch. For more information, see "[Using pagination in the REST API](https://docs.github.com/rest/using-the-rest-api/using-pagination-in-the-rest-api)."

</td></tr>
<tr><td>per_page</td><td>no</td><td>

The number of days of metrics to display per page (max 28). For more information, see "[Using pagination in the REST API](https://docs.github.com/rest/using-the-rest-api/using-pagination-in-the-rest-api)."

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/copilot/copilot-usage#get-a-summary-of-copilot-usage-for-a-team).
