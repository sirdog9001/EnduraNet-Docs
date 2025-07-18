> 🛡️ *This action requires being an [administrator](../guides/permissions.md#is_admin).*

!!! warning
    - Do not grant [can_delete_cert_hist](../guides/permissions.md) without [can_edit_cert_hist](../guides/permissions.md).[^1]
    - In order for a member to login they must have atleast 1 permission.

Member permissions are changed at the *Access Control* tab. From there, select a member using the dropdown. The checkboxes below will automatically change to reflect the permissions (or lack thereof) the user has.

To change them, simply check or uncheck the relevant boxes, and then click "Update Member Permissions"

## Changing is_admin
For security and accountability reasons changing [is_admin](../guides/permissions.md#is_admin) — and thus granting or revoking administrator status from a member — requires manual database manipulation.

[^1]: The form with the delete button that would be used by someone with `can_delete_cert_hist` requires `can_edit_cert_hist` to access. Ergo, they'd be unable to access the form to perform the deletion. This will be fixed in a future release.