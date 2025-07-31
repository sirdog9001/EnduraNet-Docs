# Release Notes

## Version 1.2.2
July 30, 2025

### Fixes
- Fixed edge case where a user with `can_delete_cert_hist` would be unable to use the permission as the form to perform deletion (`edit-cert-hist.php`) required `can_edit_cert_hist` to access. Access to form now allows _either_ permission.

## Version 1.2.1
July 19, 2025

### Features
- Link to release notes and end user documentation added to the footer.

### Fixes
- To patch a [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vector, the permission `can_edit_member` is no longer able to edit Discord IDs. Doing so now requires manual editing of the database.
- Logic added to prevent duplication of existing database records (e.g., adding the same member twice).
- Fixed issue where, due to how browsers handle time zones, dates rendered would sometimes be 1 day behind what is reflected in the database.
- Fixed issue where some of the form help text at `add-cert-hist.php` and `edit-cert-hist.php` did not match.

### Miscellaneous
- Changed the text of the hover tool-tip at `admin.php`.
- A confirmation modal now displays when adding new members. Its focus is to have the user double-check the accuracy of a submitted Discord ID.
- Help text changed at `add-member.php` and `edit-member.php` to lead to the EnduraNet documentation on how to get Discord and Steam IDs rather than third-party sites.
- The amount of characters allowed in a certification's description has been capped at 500.

### Known Issues
- User sessions cannot be remotely terminated, and thus the changing of permissions—or their revocation—will not take effect until a user logs out or their session naturally expires.
- User actions are not logged.
- Certifications cannot be set to not expire.
- Giving `can_delete_cert_hist` without `can_edit_cert_hist` makes `can_delete_cert_hist` unusable as the form where the delete functionality is located requires `can_edit_cert_hist` to access.

## Version 1.2.0
July 11, 2025

### Features
* Added new permission: `can_bypass_validate`.
    * Allows a user to bypass data validation on applicable forms (e.g. bypass "don't allow member to certify themselves" or "don't allow certification history to be in the future").
* Attempting to add certain people to the EnduraNet database may now prompt escalation to Fleff and the moderator team.
* EnduraNet will now mark someone's certification as expired if the major version number of the certification in their history does not match the up-to-date major version number.
* Reduced the width of date input fields so access to GUI-date selection wasn't on far right of the user's screen.

### Fixes
* Implemented CSRF mitigation.
* Fixed issue where the certification version in the certification history tab did not display as a decimal.
* Fixed issue where a scroll bar would appear to the right of headings on input forms.

### Miscellaneous
* Replaced alert pop-ups with class `Alert` to centralize their formatting.
* The `Delete Button` at `edit-cert-history.php` will no longer appear to those without the relevant permission. Previously, it was greyed out with a tooltip explaining why.

### Known Issues
* User sessions cannot be remotely terminated and thus the changing of permissions - or their revocation - will not take effect until a user logs out or their session naturally expires.
* User actions are not logged.

## Version 1.1.0
July 1, 2025

### Features
* Added Discord SSO OAuth2 flow to login with a Discord account and logout.
* Permissions to add, delete, and edit data tied to permissions assigned to Discord accounts.
* Font Awesome icons added to navigational tabs for aesthetic reasons.
* New pages added:
    * `admin.php` to manage permissions for those with `is_admin`.
    * `dashboard.php` which lists all forms available for those with appropriate permissions.
    * `add-member.php` to add new members to the database.
    * `edit-member.php` to edit existing members in the database.
    * `add-cert.php` to add a new certification to the database.
    * `edit-cert.php` to edit an existing certification in the database.
    * `add-cert-hist.php` to add an instance of a member being certified to the database.
    * `edit-cert-hist.php` to edit an existing record of a member being certified in the database.
* Pages updated:
    * `members.php` updated to include an error pop-up if access to EnduraNet is rejected.
    * `cert-history.php` updated to include the UID of records and a button to copy it for convenience in editing it at `edit-cert-history.php`.

### Fixes
* Fixed issue where it was not possible to have a decimal number as a certification's version number.

### Miscellaneous
* Tailwind CSS and Font Awesome added to EnduraNet libraries.
* "Powered by..." removed from footer.
* Added class `permissionChecker` to streamline authentication flow of input forms.

### Known Issues
* User sessions cannot be remotely terminated and thus the changing of permissions - or their revocation - will not take effect until a user logs out or their session naturally expires.
* User actions are not logged.
* EnduraNet does not detect and mark a certification for a member as expired if its major version changes.
* Input forms do not yet use tokens to guard against cross-site request forgery.

## Version 1.0.3
May 8, 2025

### Features
* Columns with name `Register Date` renamed to `Date Added` for clarity.
* Tagline below the title "EnduraNet" will now display a random quote curated from `#out-of-context`.
* Replaced the Endurance Coalition logo with one custom made for EnduraNet.

### Fixes
* Fixed issue where, when searching by member, only the member who most recently was given the certification would be listed as having it.
* Fixed issue where clicking `Search...` was broken on the most recent version of a site dependency.

### Miscellaneous
* Applied PHP PER 2.0 style standards to relevant code (courtesy of SierraKomodo).
* Added composer for eventual package management (courtesy of SierraKomodo).
* Replaced `config` folder with environment variables (courtesy of SierraKomodo).

## Version 1.0.2
May 1, 2025 --- Quick Urgent Fix

### Fixes
* Fixed issue where footer would clip into page content when zooming or if content length reached bottom of the view port.

## Version 1.0.1
May 1, 2025 --- Quick QOL Fixes

### Features
* Tables have been changed to have different default lengths based on what the table is.
    * Table listing members now defaults to 25 rows instead of 10.
    * Table listing the certification history now defaults to 50 rows instead of 10.
    * Tables when searching by member or by certification now default to 25 rows instead of 10.

### Fixes
* Fixed issue where bordering of table when searching by member did not match borders present on the tables of any other page.

## Version 1.0.0
May 1, 2025

EnduraNet is now ready for live data to be inserted.

### Features
* Considerable visual enhancements.
    * Navigation bar now uses a navigation bar CSS class provided by Bootstrap, eliminating the previous center-aligned black box.
    * Navigation bar now shows active page via coloring in the page name.
    * Added padding between table, navigation bar, and dropdowns for better alignment and visual fidelity.
    * Tables wrapped in a border for greater distinction.
* End user can now click a Steam ID and be directed to the individual's profile (presuming it is public).
* Database now logs who performs the final sign off on person X being certified by person Y. This information displays in expected areas.
* In relevant areas the expiry date will now change color based on whether it is expired or not.
* If a certification does not possess a recertification interval tables will output relevant text to indicate this in expected areas.
* When searching by member or certification ''specifically'', duplicate entries which may exist due to certification renewal will now not display, instead only showing the most recent.
* Added explanatory boxes to certain pages.
* A certification's prerequisite will now display in expected areas.
* When searching by member or certification, will now display more pertinent information, such as the version of the certification at the time of certification for the particular member.

### Fixes
* Fixed issue where a horizontal bar would appear at the bottom of the screen despite table width not exceeding page width.
* Fixed issue where for a split second a non-formatted version of the Datatable would appear before displaying as intended.
* Fixed issue where end user would need to select button `Search...` twice before dropdown would actually appear.
* Fixed issue where database credentials were accessible via the URL bar (courtesy of Sushiloid).

### Miscellaneous
* Standardized use of setting the DOCTYPE to HTML.
* Standardized use of PDO for SQL queries rather than a mix of that and `mysqli_query`.
* Successfully made CDN's consolidated to a header file invoked per page rather than defining per page.
* General cleanup of spacing, unused styles, duplicate invocations of `<script>`, etc.
* Version number made a PHP variable and added to `config` folder for standardization.
* Dropped table `cert_req` as, per the tech tree standard for certifications, it is not necessary to assign more than 1 certification to any 1 other certification.

## Version 0.1.0
April 29, 2025

The bare minimum viable product release of EnduraNet is now live. It can, at this time:

*   Provide a list of all members.
*   Provide a list of all certifications.
*   Provide a record of the history of certifications being performed.
*   Users can search for a specific member and see all of their certifications.
*   Users can search for a specific certification and see all members who possess it.

The visuals are still jank, and there are some core features I want to exist before I mark it v1.0 (this is mostly pedantic on my end since strict versioning for private software is meh), such as when searching by certification you get 2 separate tables so it's easy to see who is expired and who isn't, but in terms of keeping track of certifications for our current member base - especially when no certs have released yet - this'll do.

This is properly version controlled on GitHub with @sierrakomodo having access so she can make any changes or improvements that she wants, presuming she has interest and wants to help. Willing to do so the same to you @sushiloid should you care.

@fleff you will get access to the DB and advised on how to add/remove data once:

*   You actually set the time so I or @sierrakomodo can teach you SSH tunneling lmao
*   Even after SSH tunneling, I don't want anyone having DB access until regular backups are a thing.

I leave backups to you @sierrakomodo since you mentioned wanting to use duplicati.