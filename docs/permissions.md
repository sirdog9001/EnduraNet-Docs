EnduraNet uses a modular permissions model where users are assigned *individual permissions* that allow *very specific* actions.

EnduraNet determines whether an individual can login by checking to see if they have atleast 1 permission. If they do, the login will be successful and they will be able to see and access the *Data Management* tab. If not, they will be kicked back to `members.php` with a generic access denied message.

## Changing Permissions
Permissions are adjusted by administrators at the *Access Control* tab.

## Basic Permissions
These are the simple "add, edit, delete" permissions that make up the bulk of how EnduraNet functions.

| Permission | What It Does |
| :--------- | :----------- |
| `can_add_member` | Can add a new member to the database. |
| `can_edit_member` | Can edit an existing member’s information (excluding Discord ID). |
| `can_add_cert` | Can add a new certification to the database. |
| `can_edit_cert` | Can edit an existing certification’s information. |
| `can_add_cert_history` | Can add a record of someone being certified on something. |
| `can_edit_cert_history` | Can adjust the information of already existing certification records. |
| `can_delete_cert_history` | Can delete a record of someone being certified on something permanently.|

Edit and delete type permissions apply to *all* records in the database which meet the criteria. There are no restrictions on what *kinds* of such records are manipulable. For example, a person with `can_edit_member` can edit *every* member — including themselves.

## Specialized Permissions
The following are permissions which enable more nuanced behavior.

### is_admin
The permission `is_admin` is what programmatically determines if a person is an administrator or not. It grants access to the *Access Control* tab.

As a security and accountability measure this permission cannot be changed at the *Access Control* tab; it must be flipped by manually editing the database.

On the security side, it ensures that if an administrator Discord account is compromised that other adminstrators cannot be locked out. On the accountability side, `is_admin` should not be given flippantly, and it's assignment should be the product of a conversation with <abbr title="Endurance Coalition">EDC</abbr> leaders and EnduraNet's maintainer.

### can_bypass_validate
The permission `can_bypass_validate` allows the user to bypass "non-essential" validation rules when submitting forms. These are rules which apply *business logic*.

Examples include but are not limited to:

- Not allowing a record of someone being certified to be on a future date.
- Not allowing a certification to take longer than 400 days to expire.
- Not allowing the member being certified on something to be the same person who signed off on it.

Certain validation rules are classified as "essential". These ensure the *type* of data being sent is correct. As an example, some fields need numbers, not text, or the database gets angry and a scary error will appear. These rules *cannot* be bypassed with this permission.

This permission is not a perpetual state a user is in. It must be actioned by ticking a check box at the bottom of the relevant form. The check box is only visible to those with the permission.

