



# Create a SQL Server Project from a Production Data File

To create a
[SQL Server or SQL Server - Windows Authentication project SQL Server: When accessing the database from outside Value Navigator, you will need a password. SQL Server - Windows Authentication:Â When accessing the database from outside Value Navigator, Windows Authentication is used.](#), you must have
SQL Server administrator rights.

To create a SQL Server project you need to configure the connection
settings in [User Options: Connection Settings](../Options/User%20Options/User%20Options%20Connection%20Settings.md).



You must use at least SQL Server 2008 for
Value
Navigator 6 or higher databases.



It is highly recommended that you review and understand the [Fit
Settings](../Options/User%20Options/User%20Options%20Forecast%20Settings.md)
and [Import
Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md)
in the User Options before importing production data. These settings
affect how data is imported and how forecasts are created in
Value
Navigator.

To create a SQL Server (or SQL Server - Windows Authentication) project
from a production data file

1.  On the **File** menu, click **Open**.
2.  In the Project Launcher, click **Create From Import**.
3.  Browse to the production data file and click **Open**.
4.  In Project Name, type a name.
5.  In File, browse to a location to save the .vndl file (a
    Value
    Navigator-specific connection link for server-based project
    files).
6.  From the Type list, select **SQL Server** or **SQL Server - Windows
    Authentication**.
7.  In Server, type the name of the server or click to select it from
    the list.
8.  From the Res. Cat. Template list,
    select the
    [template](../Reserves%20Management/Configure%20Reserves%20Categories.md#Reserves)
    you want to use.
9.  Click **OK**.
10. In the Import Options dialog box, click **Edit** to change the
    options or click **Next** to continue.
    

    Depending on the last production dates in your data file, you might
    be asked to
    [Set the Current Month](Set%20the%20Current%20Month.md).

    
11. Click **Finish**.

A new project is created in the location you specified and
Value
Navigator opens. The new project appears in the Project Launcher
the next time you open it.
