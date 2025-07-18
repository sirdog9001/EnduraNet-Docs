??? info "Information Transparency"
    Discord's API gives EnduraNet the following information:

    - Discord username.
    - Discord ID.
    - Avatar.
    - Account 2FA status. 

EnduraNet uses Discord SSO for authentication. To login, click the "Login with Discord" button at the top right of the interface. You will be asked to authorize information.

Once you are done you should be back at the `members.php` page. The "Login with Discord" button should be replaced with your Discord information, a red logout button should be visible to the right of that, and the tab *Data Management* should be visible.

If you are kicked back with an "access denied" message it means an administrator has not given you any [permissions](../guides/permissions.md).