!!! warning
    It would be prudent to double-check that your inputs are valid. If you hit a validation rule and get sent back to a form your inputs **are not saved**.

The 2 relevant buttons at the *Data Management* tab for this are:

- Add New Certification
- Edit Existing Certification

## Fields

| Field | Data Accepted | What It Is | Visibility |
| :--------- | :----------- | :----------- | :----------- |
| Select Certification to Edit | N/A | The certification to be edited. | Edit Form |
| Name | Any | The name the certification will have. | Both |
| Creator | N/A | The member who created the certification. | Both |
| Description | Any | A short description of what the certification is. | Both |
| Status | N/A | The current status of the certification. | Both |
| Pre-requisite | N/A | If applicable, the certification that a member must have before being allowed to take the one being created. | Both |
| Source | Fully Justified URL | The raw URL to the certification's reading material. | Both |
| Version | Decimal Number | The version of the certification (likely `1.0`). | Both |
| Expiry Interval | Number | The number **of days** afterwhich the certification expires and must be renewed | Both |
| Bypass validation rules for this submission | N/A | Bypasses business logic. | Any user with [can_bypass_validate](../permissions.md#can_bypass_validate) |

Once all fields are filled, click the button at the bottom.

## Business Logic
For user convenience the following conditions apply. These are enforced programmatically and will result in a kick-back to the form if violated.

- `Expiry Interval` may not equal or exceed 400 days.