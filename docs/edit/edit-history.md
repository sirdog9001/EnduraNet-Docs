!!! warning
    It would be prudent to double-check that your inputs are valid. If you hit a validation rule and get sent back to a form your inputs **are not saved**.

The 2 relevant buttons at the *Data Management* tab for this are:

- Add Someone Being Certified
- Edit Existing Certification History

Deletions occur at "Edit Existing Certification History".

| Field | Data Accepted | What It Is | Visibility |
| :--------- | :----------- | :----------- | :----------- |
| Certification History to Edit | N/A | The [UID](../viewing-data.md#certification-history) of the certification record. | Edit Form |
| Date Member was Certified | N/A | The date the certification happened. | Both |
| Member Being Certified | N/A |  The member getting credited with a certification. | Both |
| Certifying Member | N/A | The member who performed the certification of the `Member Being Certified`. | Both |
| Member Who Signed Off | N/A | The member — traditionally someone in a leadership role — who sanity checked that the certification procedure was more-or-less adhered to for the `Member Being Certified`. | Both |
| Certification | N/A | The certification that `Member Being Certified` is getting credited as having. | Both |
| Certification Version | Decimal Number | The version of the certification as it was on the ` Date Member was Certified`. | Add Form (read-only)<br/>Edit Form (editable) |
| Bypass validation rules for this submission | N/A | Bypasses business logic. | Any user with [can_bypass_validate](../permissions.md#can_bypass_validate) |

## Business Logic
For user convenience the following conditions apply. These are enforced programmatically and will result in a kick-back to the form if violated.

- `Member Being Certified` and `Certifying Member` may not be the same.
- `Member Who Signed Off` may not be the same as `Member Being Certified` or `Certifying Member`.
- `Date Member was Certified` may not be in the

## Deletion
Deletion requires [can_delete_cert_history](../permissions.md#basic-permissions). If the user looking at the form has it a "Delete Record" button will be adjacent to the "Edit Record" button. A `Certification History to Edit` will need to be selected first before clicking "Delete Record".