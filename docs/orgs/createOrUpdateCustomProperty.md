---
name: Create or update a custom property for an organization
example: octokit.rest.orgs.createOrUpdateCustomProperty({ org, custom_property_name, value_type })
route: PUT /orgs/{org}/properties/schema/{custom_property_name}
scope: orgs
type: API method
---

# Create or update a custom property for an organization

Creates a new or updates an existing custom property that is defined for an organization.

To use this endpoint, the authenticated user must be one of:

- An administrator for the organization.
- A user, or a user on a team, with the fine-grained permission of `custom_properties_org_definitions_manager` in the organization.

```js
octokit.rest.orgs.createOrUpdateCustomProperty({
  org,
  custom_property_name,
  value_type,
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
<tr><td>custom_property_name</td><td>yes</td><td>

The custom property name

</td></tr>
<tr><td>value_type</td><td>yes</td><td>

The type of the value for the property

</td></tr>
<tr><td>required</td><td>no</td><td>

Whether the property is required.

</td></tr>
<tr><td>default_value</td><td>no</td><td>

Default value of the property

</td></tr>
<tr><td>description</td><td>no</td><td>

Short description of the property

</td></tr>
<tr><td>allowed_values</td><td>no</td><td>

An ordered list of the allowed values of the property.
The property can have up to 200 allowed values.

</td></tr>
<tr><td>values_editable_by</td><td>no</td><td>

Who can edit the values of the property

</td></tr>
  </tbody>
</table>

See also: [GitHub Developer Guide documentation](https://docs.github.com/rest/orgs/custom-properties#create-or-update-a-custom-property-for-an-organization).
