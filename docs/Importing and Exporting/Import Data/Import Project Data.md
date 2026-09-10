



# Import Project Data

Use this procedure to import any of the following items:

| Price Decks Batch Definitions Change Record Categories Companies Countries Currencies Custom Data Fields Fiscal Regimes Facilities Hierarchies Meter Stations | Prices, Royalties, Tax Rates, and Price Sets Project Options Scenarios Summary Types Tax Pools Transportation Area Bulk Well Schedules Rollups Type Wells Wells and Groups Plans |
| --- | --- |


To import custom data in a spreadsheet (production data or custom text
field data in an .xlsx, .csv, or .prd format) see
[Import Spreadsheet Data](../Spreadsheet%20Import/Import%20Spreadsheet%20Data.md) .

To import wells based on a text file, see
[Import Wells from a Well List (text file)](Import%20Wells%20from%20a%20Well%20List%20text%20file.md) .

You can also import User and Project Options from the
Options dialog box (from the **Tools**
menu, select **Options**). See
[Import Project and User Options](Import%20Project%20and%20User%20Options.md).



If you are importing entities from another
Value
Navigator project, see
[Merge Projects](../Merge%20Projects.md)
for important guidelines.



To import data

1.  On the **File**menu select **Import**\&gt;
    File.
2.  Select **Import** from an existing file and click ![](../../Images/Import-Project-Data-1.jpg) to
    browse to the file.
3.  Select the file and click **Open**.
4.  Click **Next** and then click Finish.

## Note on Importing Change Records

Change records are only imported when:

- The **Include Change Records and Opening Balances** option was
  selected during the export.
- The target project is posted and the last posted date in the target
  project and XML file match. Change Records for the current period
  (after the last posted date) are imported.
- The target project is not posted and the XML file does not have a last
  posted date record.
