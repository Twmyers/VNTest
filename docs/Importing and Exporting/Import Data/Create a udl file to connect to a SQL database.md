

# Create a .udl file to connect to a SQL database

Val Nav uses a .udl (Universal Data Link) file to connect to a SQL
Server hub.



If the text file is not recognized as a .udl file, you may need to
change your Windows Explorer view to display file extensions.



To create a .udl file

1.  Use Notepad or something similar to create an empty text file and
    save it as *\.udl* with UTF Encoding set to
    UTF-16LE. Save this file on a network
    in a place all users can access.
    
2.  In File Explorer, right-click *\.udl* and select
    Properties.
3.  On the Provider tab, select
    Microsoft OLE DB Provider for SQL
    Server.
4.  On the Connection tab, complete the
    following: 
    | Step | Description |
| --- | --- |
| Server name | Select or enter the name of the server on which the SQL database is hosted. |
| Server login information | Enter information to log on to the server. This user name and password is for the connection to the SQL database. Blank password checkbox: Select this if ValNav users will be prompted for the database schema password when they update production. Allow saving password checkbox: Select this if the DBA wants to let all ValNav users access the production update without being prompted for the password. |
| Database on the server | Select the database on the server. This is the name of the specific database that is storing the information to be retrieved. |

5.  Click Test Connection.
