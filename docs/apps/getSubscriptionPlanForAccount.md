---
name: Get a subscription plan for an account
example: octokit.rest.apps.getSubscriptionPlanForAccount({ account_id })
route: GET /marketplace_listing/accounts/{account_id}
scope: apps
type: API method
---

# Get a subscription plan for an account

Shows whether the user or organization account actively subscribes to a plan listed by the authenticated GitHub App. When someone submits a plan change that won't be processed until the end of their billing cycle, you will also see the upcoming pending change.

GitHub Apps must use a [JWT](https://docs.github.com/apps/building-github-apps/authenticating-with-github-apps/#authenticating-as-a-github-app) to access this endpoint. OAuth apps must use [basic authentication](https://docs.github.com/rest/authentication/authenticating-to-the-rest-api#using-basic-authentication) with their client ID and client secret to access this endpoint.

```js
octokit.rest.apps.getSubscriptionPlanForAccount({
  account_id,
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
    <tr><td>account_id</td><td>yes</td><td>

account_id parameter

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/apps/marketplace#get-a-subscription-plan-for-an-account).
