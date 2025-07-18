# Welcome to EnduraNet's Documentation

**The documentation for EnduraNet — the Endurance Coalition's information management system for Arma 3.**<br/>
*Current version: v1.2.0 · Last updated: July 11, 2025*

---
## Common Actions

<div class="grid cards" markdown>

-   __Find out if someone has a certification?__

    ---

    See [<abbr title="Anyone Can Do This">🌐</abbr> Check Certification Status](how-to/check-cert-status.md).

-    __Create a record of someone being certified?__

    ---

    See  [<abbr title="Permission Gated">🔑</abbr> Add a New Certification Event](how-to/add-new-history.md).

-   __Change someone's permissions?__

    ---

    See [<abbr title="Administrator Only">🛡️</abbr> Change Permissions](how-to/change-perms.md).

</div>

---

## What's new in v1.2.0?

* Added new permission: `can_bypass_validate`.
    * Allows a user to bypass data validation on applicable forms (e.g. bypass "don't allow member to certify themselves" or "don't allow certification history to be in the future").
* Attempting to add certain people to the EnduraNet database may now prompt escalation to Fleff and the moderator team.
* EnduraNet will now mark someone's certification as expired if the major version number of the certification in their history does not match the up-to-date major version number.
* Reduced the width of date input fields so access to GUI-date selection wasn't on far right of the user's screen.

---

## Need Help?
| Issue Type               | How to Report                                                                 |
|--------------------------|-------------------------------------------------------------------------------|
| 🐞 **General Bugs**       | DM Sirdog or ping in `EnduraNet (Cert DB)` thread of `dev-ops` forum (EDC Discord).                   |
| 🔒 **Security/Privacy Issues**    | DM Sirdog or email `enduranetsecurity.dastardly057@passmail.net` ([Proton Mail](https://proton.me/)).           |
| ❓ **Usage Questions**    | Check [How to Use](viewing-data.md) or ask in `EnduraNet (Cert DB)` thread .                              |
| ✨ **Feature Requests**   | Ask in `EnduraNet (Cert DB)` thread.    |