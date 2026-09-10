



# Gather Database Statistics

Gather Database Statistics enables a user to optimize the performance of
Value
Navigator Oracle and SQLite projects. Gathering database
statistics can increase the speed of many operations in
Value
Navigator, such as economic calculations, batch operations, and
export/import. It accomplishes this by gathering statistics about tables
and indices which enables the query optimizer to make better query
planning choices.

Database Statistics are automatically gathered during an economic
calculation when a folder level or consolidation calculation requires
the calculation of more than 500 entities. In addition, the statistics
for a particular table are only calculated if there were no previous
statistics or the number of rows stored with the existing statistics
differs by more than 10% of the actual number of rows in the table.

To gather database statistics, click **Gather Database** **Statistics**
in the **Administration** menu while in an Oracle or SQLite project.

To disable the automatic gathering of database statistics

1.  Open the **Eni.ValueNavigator.config** file located in the
    Value
    Navigator installation folder.
2.  Set the gather_statistics setting to **False**.

Once you set the **gather_statistics** setting to false, statistics are
no longer automatically gathered.

To gather database statistics, click **Gather Database** **Statistics**
in the **Administration** menu while in an Oracle or SQLite project.
