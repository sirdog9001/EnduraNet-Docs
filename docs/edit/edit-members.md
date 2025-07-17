!!! warning
    It would be prudent to double-check that your inputs are valid. If you hit a validation rule and get sent back to a form your inputs **are not saved**.

The 2 relevant buttons at the *Data Management* tab for this are:

- Add New Member
- Edit Existing Member

## Fields

| Field | Data Accepted | What It Is | Visibility |
| :--------- | :----------- | :----------- | :----------- |
| Select Member to Edit | N/A | The member who's information will be edited. | Edit Form |
| Date Added | N/A | This simply records for posterity the date this member was added to EnduraNet. | Both |
| Name |Any| This is going to be the common name for this person. | Both |
| Discord ID |Number| This is the Discord ID for the person. | Add Form (editable)<br/>Edit Form (read-only) |
| Steam ID |Number| This is the Steam ID for the person. | Both |

Once all fields are filled, click the button at the bottom.

## Getting a Discord ID
!!! info
    To ensure that the number you have is actually a Discord ID check it against the [Discord.id](https://discord.id) website.
A Discord ID is a long-number value which *uniquely* identifies a person's Discord account against all others. This field is *extremely important* for EnduraNet as it is part of the authentication process to login and be assigned permissions.

To get a Discord ID, do the following:

1. Click the `User Settings` cog to the right of the `Mute` and `Deafen` icons.
2. Click `Advanced` under the *App Settings* list.
3. Check `Developer Mode`.
4. Exit user settings.
5. Find any message which has been sent by the user in question.
6. Right click their *name*.
7. Select option `Copy User ID`.

An example of a proper Discord ID is `137356883664175104`.

## Getting a Steam ID
!!! warning
    It is important that the Steam ID be in x64 format (e.g starts with `7656`). The old format (e.g `STEAM_0:0:47830396`) is not acceptable.

A Steam ID is a long-number value which *uniquely* identifies a person's Steam account against all others. This field is important so that the hyperlink to the member's Steam profile at the [members tab](../viewing-data.md#members) functions.

To get a Steam ID, do the following:

1. Navigate to the Steam profile of the person either in your browser or in the Steam app.
    1. There should be a URL that looks like: `https://steamcommunity.com/id/<stuff>`.
2. The `<stuff>` is either a number, likely starting with `765`, or it's a custom tag which users can make.
    1. If it's the number, **that is the ID**. Copy that and paste it in the `Steam ID` field. You are done.
    2. If it's the tag, keep reading.
3. Copy the entire URL.
4. Go to [SteamID.io](https://steamid.io/lookup/).
5. Paste the entire URL into the `input...` bar and click "lookup".
6. Copy the `steamID64` field. Paste it into the `Steam ID` field. You are done.

## Deletion
Deletion of members is not supported as they are necessary to avoid data corruption. It is on the roadmap to implement systems to allow members which have been sunset to be hidden from view. 