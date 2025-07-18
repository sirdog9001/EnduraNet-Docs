In the context of EnduraNet and the [can_bypass_validate](permissions.md#can_bypass_validate) permission, *business logic* is any validation rule that exists for a purpose that *is not* to protect the database from errors.

Examples include but are not limited too:

- Not allowing a record of someone being certified to be on a future date.
- Not allowing a certification to take longer than 400 days to expire.
- Not allowing the member being certified on something to be the same person who signed off on it.