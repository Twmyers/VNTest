



# Upgrading to Value Navigator 2020

Do not upgrade projects to by exporting an XML file from the previous
version and importing it into
2020.
To guarantee all data is properly upgraded, upgrade your database by
opening the original version in Value Navigator
2020,
which starts an automatic upgrade. If you wish to migrate to a different
database platform, first upgrade your database to
2020.
Then export the XML from
2020and
import it into the new platform.



A Value Navigator 6.x Oracle or SQL Server database will upgrade “in
place” to Value Navigator
2020,
meaning that once it has been upgraded to
2020,
it can no longer be run in the previous version. We therefore recommend
you make a backup of 6.x databases before upgrading them to
2020.



When you open an older
Value
Navigator project (version 6 or higher) in
Value
Navigator2020,
it is converted to
2020automatically.
When you upgrade a SQLite database, a backup of the original project is
automatically created and saved in the same folder.



SQL Server and Oracle databases upgrade "in place" which means the
upgraded project overwrites the older project. Therefore, you should
have your database administrator create a backup of server projects
before you upgrade them.\





If you are upgrading a
Value
Navigator 5.2 project, please contact
[Value Navigator Support](../../Support.md).



## Special Upgrade Notes for 2019 and Later

### Password Requirements Change

If your password in the project you're upgrading contains non-ASCII
characters, you must change it to contain only ASCII characters before
you upgrade a project to
Value
Navigator 2019 or later. If you upgrade a project without
updating your password to contain only ASCII characters, you'll be
locked out of the project. See
[ValNav 2019 Password Requirements](ValNav%202019%20Password%20Requirements.md) for more
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
