!!! warning
    While it is possible to do this, do not give `can_delete_cert_hist` without also giving `can_edit_cert_hist`. The deletion permission simply makes a button visible at `edit-cert-hist.php` and that page requires `can_edit_cert_hist` to access. 
    
    In other words, if you give delete without editing, the user functionally cannot use the permission.

    This is set to be rectified in the next feature release.

Permissions are changed by visiting the *Access Control* tab to the right of the *Data Management* tab.

From here, you will use the `Select Member to Edit` box to choose the member who's permissions you'd like to edit. Once you do so, their permissions (if they have any) will automatically reflect in the checkboxes below.

The checkboxes are fairly straight-forward with relevant explanatory text. To give or revoke a permission, check or uncheck the relevant box. Once done, click the "Update Member Permissions" button.

## Permission Updates
Due to how sessions are handled by EnduraNet, once a member logs in, their permissions remain static until they log out and back in. It is on the roadmap to make this more dynamic.