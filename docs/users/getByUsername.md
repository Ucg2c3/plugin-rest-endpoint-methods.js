---
name: Get a user
example: octokit.rest.users.getByUsername({ username })
route: GET /users/{username}
scope: users
type: API method
---

# Get a user

Provides publicly available information about someone with a GitHub account.

If you are requesting information about an [Enterprise Managed User](https://docs.github.com/enterprise-cloud@latest/admin/managing-iam/understanding-iam-for-enterprises/about-enterprise-managed-users), or a GitHub App bot that is installed in an organization that uses Enterprise Managed Users, your requests must be authenticated as a user or GitHub App that has access to the organization to view that account's information. If you are not authorized, the request will return a `404 Not Found` status.

The `email` key in the following response is the publicly visible email address from your GitHub [profile page](https://github.com/settings/profile). When setting up your profile, you can select a primary email address to be public which provides an email entry for this endpoint. If you do not set a public email address for `email`, then it will have a value of `null`. You only see publicly visible email addresses when authenticated with GitHub. For more information, see [Authentication](https://docs.github.com/rest/guides/getting-started-with-the-rest-api#authentication).

The Emails API enables you to list all of your email addresses, and toggle a primary email to be visible publicly. For more information, see [Emails API](https://docs.github.com/rest/users/emails).

```js
octokit.rest.users.getByUsername({
  username,
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
    <tr><td>username</td><td>yes</td><td>

The handle for the GitHub user account.

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/users/users#get-a-user).
