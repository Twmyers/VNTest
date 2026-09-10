

# Create a New SQL Server Database 2008, 2008 R2 (User Authentication)

SQL Server 2008 and 2008 R2 can support user authentication, however,
the following steps are needed to convert the database. Follow the
process as for a Windows authenticated database, then modify the
database properties:

1.  Using the SQL Server Management Studio, connect to the database
    using a DBA account.
2.  View the properties of the database and ensure it is configured as
    ‘SQL Server and Windows Authentication mode’.
3.  Click OK to close the Properties dialog.
4.  In the Security section of the database, right-click the Logins
    folder and select New Login.
5.  The Login dialog appears.
6.  Enter the Login name for the user that
    Value
    Navigator will connect to the database as (the
    Value
    Navigator standard is to name it the same name as the
    Value
    Navigator project you will use it for, vn_projectname).
7.  Choose ‘SQL Server authentication’ option.
8.  Enter the Password for the database.
9.  Review the state of the three options: enforced password policy,
    enforce password expiration, user must change password at next
    login. You can choose to leave them checked, but the
    Value
    Navigator standard is to uncheck them.
10. Select the ‘Default database’ as the project you are converting.
11. Go to the User Mapping page in the Login dialog.
12. Put a checkmark in the Map column of the project you are converting.
13. Set its Default Schema to \[dbo\].
14. In the Login dialog, check db_owner in the list of “Database role
    membership” for the project.
15. Click OK.

The login you have just created will only have access to the
Value
Navigator project you are converting. Now create a new VNDL to
use to connect to the database:

1.  Open Value
    Navigator.
2.  Close the Project Launcher
3.  Select File \&gt; Edit or Create Project Connection File. The ‘Project
    Connection Information’ dialog appears.
4.  Select a name and location for the new VNDL.
5.  Select Project Type = SQL Server.
6.  Choose the correct Server.
7.  Enter the Project you are converting.
8.  Enter the User and Password information for the new authentication
    database you just created.
9.  Test the Connection and click Save.

The new VNDL file, which accesses the new project that uses SQL Server
authentication, is now created. Browse to this VNDL from the Project
Launcher to open this database.
Value
Navigator uses the new user to connect to this SQL Server
database. Because the password is encrypted in the VNDL file, users can
connect to the database via
Value
Navigator without requiring the database password, but they
cannot access the password in order to connect to the database by other
applications.
