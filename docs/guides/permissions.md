EnduraNet's <abbr title="Create, read, update, delete">CRUD</abbr> implementation is built on a modular individual-user permissions model. Rather than creating roles which can perform a variety of actions, instead, individual actions are assigned to specific members. 

Data manipulation is broken down into being able to **add** new information, **edit** existing information, or **delete** existing information. This is further broken down based on the kind of data: members, certifications, and certification history.

The assignment of permissions is done by administrators at the *Access Control* tab. See [Changing Permissions](../how-to/change-perms.md) for how to do so.

The permissions are grouped into 2 categores.

- Basic
- Administrative

## Basic Permissions
These are the self-contained and self-explanatory permissions that allow adding, editing, or deleting certain kinds of information.

| Permission            | What It Does                                                                 |
| :--------------------- | :-------------------------------------------------------------------------- |
| can_add_member         | Can add a new member to the database.                                       |
| can_edit_member        | Can edit an existing member’s information (excluding Discord ID).           |
| can_add_cert           | Can add a new certification to the database.                               |
| can_edit_cert          | Can edit an existing certification’s information.                          |
| can_add_cert_hist   | Can add a record of someone being certified on something.                  |
| can_edit_cert_hist  | Can adjust the information of already existing certification records.       |
| can_delete_cert_hist| Can delete a record of someone being certified on something permanently.    |

Edit and delete type permissions apply to *all* records in the database which meet the criteria. There are no restrictions on what *kinds* of such records are manipulable. For example, a person with `can_edit_member` can edit *every* member — including themselves.

## Administrative Permissions
These are *any other kind* of permission which don't fall into the "Basic Permissions" category.

### is_admin
Determines if a person is an administrator or not. It grants access to the *Access Control* tab.

### can_bypass_validate
Allows a user to on applicable forms to bypass [business logic](business-logic.md). Validation rules that protect the data integrity of the database are not bypassable.

