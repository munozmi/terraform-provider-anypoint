---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "anypoint_user Resource - terraform-provider-anypoint"
subcategory: ""
description: |-
  Creates a `user` for your org. 
  
  N.B: you can use a username only once even after it's deleted.
---

# anypoint_user (Resource)

Creates a `user` for your org. 

**N.B:** you can use a username only once even after it's deleted.

## Example Usage

```terraform
resource "anypoint_user" "user" {
  org_id = var.root_org
  username = "my_unique_username01"
  first_name = "terraform"
  last_name = "provider"
  email = "terraform@provider.com"
  phone_number = "0756224452"
  password = "my_super_secret_pwd"
}

output "user" {
  value = data.anypoint_user.user
  sensitive = true
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **email** (String, Sensitive) The email of this user.
- **first_name** (String, Sensitive) The firstname of this user.
- **last_name** (String, Sensitive) The lastname of this user.
- **org_id** (String) The master organization id where the user is defined.
- **password** (String, Sensitive) The password of this user.
- **phone_number** (String, Sensitive) The phone number of this user.
- **username** (String) The username of this user.

### Optional

- **last_updated** (String) The last time this resource has been updated locally.

### Read-Only

- **contributor_of_organizations** (Set of Map of String) The list of organizations this user has contributed to.
- **created_at** (String) The time when the user was created.
- **deleted** (Boolean) Whether this user is deleted
- **enabled** (Boolean) Whether this user is enabled
- **id** (String) The unique id of this user generated by the anypoint platform.
- **idprovider_id** (String) The identity provider id
- **is_federated** (Boolean) Whether this user is federated.
- **last_login** (String) The last time this user logged in.
- **member_of_organizations** (Set of Map of String) The user's list of organizations membership
- **mfa_verification_excluded** (Boolean) Whether MFA verification is excluded for this user
- **mfa_verifiers_configured** (String) The MFA configured for this user.
- **organization** (Map of String) The organization information
- **organization_id** (String) The master organization id where the user is defined.
- **organization_preferences** (Map of String) The preferences of the user within the organization.
- **properties** (String) The user's properties.
- **type** (String) The type of user.
- **updated_at** (String) The last time this user was updated.


