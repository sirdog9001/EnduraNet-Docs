> 🛡️ *This action requires being an [administrator](../guides/permissions.md#is_admin).*

Member permissions are changed at the *Access Control* tab. From there, select a member using the dropdown. The checkboxes below will automatically change to reflect the permissions (or lack thereof) the user has.

To change them, simply check or uncheck the relevant boxes, and then click "Update Member Permissions".

The revocation of *all* permissions will also take away a member's ability to login. Granting atleast 1 permission grants the ability *to* login.

## Changing is_admin
For security and accountability reasons changing [is_admin](../guides/permissions.md#is_admin) — and thus granting or revoking administrator status from a member — requires manual database manipulation.

A natural consequence of this is that an administrator cannot revoke another administrator's ability to login. EnduraNet counts [is_admin](../guides/permissions.md#is_admin) as a permission for login purposes. This is by design.