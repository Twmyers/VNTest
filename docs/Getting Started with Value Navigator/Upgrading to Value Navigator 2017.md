



# Upgrading to Value Navigator 2017

When you open an older
Value
Navigator project (version 6 or higher) in
Value
Navigator 2017, it is converted to 2017 automatically. When you
upgrade a SQLite database, a backup of the original project is
automatically created and saved in the same folder.



SQL Server and Oracle databases upgrade "in place" which means the
upgraded project overwrites the older project. Therefore, you should
have your database administrator create a backup of server projects
before you upgrade them.\



If you are upgrading a
Value
Navigator 5.2 project, please contact
[Value Navigator Support](../../Support.md).

## Upgrade Changes

If you upgrade to the 64-bit version of
Value
Navigator and are using a ..udl or a ..vnudl to connect to a data
provider (e.g. a PPDM hub, or a database with capital actuals), you will
need to change the name of the provider in those files from *MSDORA.1*
to *Devart.Data.Oracle*. To make the change, open the .udl/.vnudl file
in a text editor, such as Notepad, and replace the *Provider* in the
file.

We also recommended this with Windows versions 8 and up.

## Special Upgrade Notes for 2019

### Password Requirements Change

If your password in the project you're upgrading contains non-ASCII
characters, you must change it to contain only ASCII characters before
you upgrade a project to
Value
Navigator 2019. If you upgrade a project without updating your
password to contain only ASCII characters, you'll be locked out of the
project. See [ValNav 2019 Password Requirements](ValNav%202019%20Password%20Requirements.md) for more
information.

### Reserves Categories Queries

With the ability to
[Rename Reserves Categories](../Entity%20Management/Rename%20Reserves%20Categories.md) in
Value
Navigator 2019, the reserves category names formerly stored in
the CODE_LOOKUP table are no longer used, and those rows will be deleted
on upgrade. Queries referencing the RESERVE_CATEGORY code type in that
table will need to be rewritten to instead join on the
FISC_RESERVE_CATEGORY table.
