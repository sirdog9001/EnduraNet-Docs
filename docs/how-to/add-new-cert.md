> 🔑 *This action requires being logged in with [can_add_cert](../guides/permissions.md#basic-permissions).*

!!! info "Business Logic"
    The following [business logic](../guides/business-logic.md) apply to certifications. Violation without using the bypass will cause the submission to be rejected. **Inputs are not saved when submissions are rejected.**
    
    - `Expiry Interval` cannot meet or exceed 400 days.
    - `Description` cannot exceed 500 characters. *This cannot be bypassed.*

To add a new certification, go to the *Data Management* tab and click the `Add New Certification` button.

You will be shown a form with the following fields.

| Field | Data Accepted | What It Is | Visibility |
| :--------- | :----------- | :----------- | :----------- |
| Date Added | N/A | EnduraNet will set the date the certification was added to the database as this date.  |
| Name | Any | The name the certification will have. |
| Creator | N/A | The member who created the certification. |
| Description | Any | A short description of what the certification is. |
| Status | N/A | The current status of the certification. |
| Pre-requisite | N/A | If applicable, the certification that a member must have before being allowed to take the one being created.[^1] |
| Source | Fully Justified URL | The raw URL to the certification's reading material. |
| Version | Decimal Number | The version of the certification (likely `1.0`). |
| Expiry Interval | Number | The number **of days** afterwhich the certification expires and must be renewed |
| Bypass validation rules for this submission | N/A | Bypasses business logic. **Only visible to those with `can_bypass_validate`** |

Once you are done, click `Add Certification`. 

[^1]: This is as of EnduraNet v1.2.0 not enforced programmatically.