

# Create a New SQL Server Database (Windows Authentication) for Value Navigator

1.  Create an empty database ‘NEWUSER’ using ‘SQL server – Windows
    Authentication’ on a SQL Server instance.
2.  Create a new Login for the Windows User/Group on the SQL Server
    instance. The Login does not require additional Server Roles aside
    from public.
3.  Create a User Mapping for the Windows User/Group on the newly
    created empty ‘NEWUSER’ database. The User Mapping requires the
    following database-level roles:
    1.  db_datareader (connect to and use project databases)
    2.  db_datawriter (connect to and user project databases)
    3.  db_ddladmin (create project databases)
