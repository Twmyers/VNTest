

# Create a New SQL Server Database (User Authentication – SQL Server 2012+)

User authenticated SQL Server projects using SQL Server 2012 and newer
can be created from ValNav with no other authentication modifications.

1.  Create an empty database ‘NEWUSER’ using ‘SQL Server’ on a SQL
    Server instance. See ‘Create a new
    Value
    Navigator Project’ below.
2.  Create a new Login for the Windows User/Group on the SQL Server
    instance. The Login does not require additional Server Roles aside
    from public.
3.  Create a User Mapping for the Windows User/Group on the newly
    created empty ‘NEWUSER’ database. The User Mapping requires the
    following database-level roles:
    1.  db_datareader (Connect and use project databases)
    2.  db_datawriter (Connect and use project databases)
    3.  db_ddladmin (Create project databases)



Logins for SQL Server users who will be connecting to DBA created
databases in order to create
Value
Navigator projects must have the db_ddladmin role in addition to
db_datareader and db_datawriter. Logins for users who will be connecting
to and using existing project databases only need the db_datareader and
db_datawriter roles.
