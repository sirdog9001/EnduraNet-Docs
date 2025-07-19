> 🔑 *This action requires being logged in with [can_edit_cert_hist](../guides/permissions.md#basic-permissions).*

!!! info "Business Logic"
    The following [business logic](../guides/business-logic.md) apply to certification history. Violation without using the bypass will cause the submission to be rejected. **Inputs are not saved when submissions are rejected.**
    
    - `Member Being Certified` may not be the same member as `Certifying Member`.
    - `Member Who Signed Off` may not be the same member as `Member Being Certified` **or** `Certifying Member`.
    - `Date Member was Certified` may not be a date in the future.

To edit existing certification history, go to the *Data Management* tab and click the `Existing Certification History` button.

You will be shown a form with the following fields. 

| Field | Data Accepted | What It Is | Visibility |
| :--------- | :----------- | :----------- | :----------- |
| Certification History to Edit | N/A | The [UID](search-history.md) of the certification record. |
| Date Member was Certified | N/A | The date the certification happened. |
| Member Being Certified | N/A |  The member getting credited with a certification. | 
| Certifying Member | N/A | The member who performed the certification of the `Member Being Certified`. |
| Member Who Signed Off | N/A | The member — traditionally someone in a leadership role — who sanity checked that the certification procedure was more-or-less adhered to for the `Member Being Certified`. |
| Certification | N/A | The certification that `Member Being Certified` is getting credited as having. |
| Certification Version | Decimal Number | The version of the certification as it was on the ` Date Member was Certified`. |
| Bypass validation rules for this submission | N/A | Bypasses business logic. **Only visible to those with `can_bypass_validate`** |

Once you are done, click `Add Certification History`. 

## Finding a Record 
Because there is not an obvious name for certification history records a record's [UID](search-history.md) is used for the selection dropdown. This is a unique identifier assigned to every instance of a certification event. 

To find the UID of the record you'd like to manipulate go to the *Certification History* tab and use the table's search bar. Once you've found the record, copy or remember it's UID, then return to the editing form. You'll select that number for the `Certification History to Edit` field.
