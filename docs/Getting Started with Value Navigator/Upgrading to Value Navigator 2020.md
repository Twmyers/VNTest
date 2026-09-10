



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
