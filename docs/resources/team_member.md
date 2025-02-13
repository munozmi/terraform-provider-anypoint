---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "anypoint_team_member Resource - terraform-provider-anypoint"
subcategory: ""
description: |-
  Assignes a `user` to a `team` for your `org`.
---

# anypoint_team_member (Resource)

Assignes a `user` to a `team` for your `org`.

## Example Usage

```terraform
resource "anypoint_team_member" "team_member" {
  org_id = var.root_org
  team_id = anypoint_team.team.id
  user_id = anypoint_user.user.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **org_id** (String) The master organization id where the team is defined.
- **team_id** (String) The id of the team. team_id is globally unique.
- **user_id** (String) The owner id

### Optional

- **last_updated** (String) The last time this resource has been updated locally.
- **membership_type** (String) Whether the member is a regular member or a maintainer. Only users may be team maintainers. Enum values: member, maintainer

### Read-Only

- **created_at** (String) The member team assignment creation date
- **id** (String) The unique id of this team membership composed by `org_id`_`team_id`_`user_id`_members
- **identity_type** (String) The member's identity type.
- **is_assigned_via_external_groups** (Boolean) Whether the member was assigned to the team via a external group mapping
- **name** (String) The name of the team
- **updated_at** (String) The member team assignment update date


