

# ValNav 2019 Password Requirements

If your password contains non-ASCII characters, you must change it to
contain only ASCII characters before you upgrade a project to
Value
Navigator 2019. If you upgrade a project without updating your
password to contain only ASCII characters, you'll be locked out of the
project.

Value
Navigator 2019 contains security changes to its password-hashing
algorithm. Previously, we were hashing all passwords as ASCII text, but
now are hashing with a UTF-8 algorithm. This means that the password
hashes for non-ASCII characters (accented letters, Cyrillic characters,
etc.) have changed, and those passwords will not be validated in
upgraded databases.



Active Directory (single sign-on) users are not affected.



To avoid this, you must change your password in the prior version of
ValNav before doing the upgrade. Change
your password to one using only ASCII characters, upgrade the database,
and then change it to a secure password of your choice. We are unable to
determine which passwords have accented characters, as our password
hashes are one-direction only.

Updating your password is especially important for admin users (those
users who can manage security settings in multi-user databases), as
admins can reset the password for other users, helping them through this
change.

If you upgrade your database without changing your password and become
locked out, please contact
[Value Navigator Support](../../Support.md).
