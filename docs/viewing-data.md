# The Tabs
When you first visit EnduraNet you are plopped at the "Members" tab, one of 6 total tabs that are visible to all site visitors. 

All tables are generated using the [Datatables](https://datatables.net/) framework. Long story short, it's why they are paginated and have a search bar. The search bar can be used to search on *any* column.

## Members
This is a simple list of all members that EnduraNet is aware of. Not all members of the <abbr title="Endurance Coalition">EDC</abbr> Discord are added indiscriminately. People are typically added as they take interest in Arma 3 and thus tracking their information becomes necessary.

The displayed table is fairly straight forward. Clicking on a Steam ID will lead you to the relevant member's Steam profile. Whether or not any information is visible is dependent on the member's Steam privacy settings.

## Certifications
This is a list of all certifications available. *Most* of the columns are self-explanatory.

| Column | Meaning |
| :--------- | :----------- |
| Source | A hyperlink to the certification's review material. |
| Version | The current version of the certification. See the EDC wiki page on [the Arma 3 metagame](https://wiki.edcgaming.org/Arma_3_metagame) for more information about this. |
| Expires After | The number of days afterwhich the certification must be renewed. |

## Certification History
This is a raw table of every single certification record to exist.

| Column | Meaning |
| :--------- | :----------- |
| UID | Used by those with [can_edit_cert_hist](permissions.md#basic-permissions) or [can_delete_cert_hist](permissions.md#basic-permissions) to find a particular record to manipulate. |
| Member Certified | The member getting credited with a certification. |
| Certifying Member | The member who performed the certification of the `Member Certified`. |
| Signed Off By | The member — traditionally someone in a leadership role — who sanity checked that the certification procedure was more-or-less adhered to for the `Member Certified`. |
| Certification | The certification that `Member Certified` is getting credited as having. |
| Certification Date | The date the certification happened. |
| Certified on Version | The version of the certification as it was on the `Certification Date`. |
| Actions | A button to quickly copy the `UID`. |

## Search...
This dropdown allows you to specify if you want to search `By Member` or `By Certification`. 

- `By Member` will allow you to specify a member from a dropdown, see every certification they have, and whether it is valid or not.
- `By Certification` will allow you to specify a certification, see every member who's ever taken it, and whehther it is valid for them or not.

The columns for the tables on each page differ only slightly from the [Certification History](#certification-history) tab. 

A new column, "Expires On", exists for these pages. The date is determined automatically by EnduraNet by calculating the `Certification Date` against the certification's `Expires After` column.