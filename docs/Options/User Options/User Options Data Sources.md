

# User Options Data Sources

Before you can import data from IHS, GeoLogic, a corporate data hub (for
daily data or
Execute)
you must set up a connection. See [Configure an External Data Source](../../Importing%20and%20Exporting/Import%20Data/Configure%20an%20External%20Data%20Connection.md).

### Data Source

- **Profile:** By default, IHS, GeoLogic, Daily Data, and Actual Capital
  Costs
  (Execute)
  are available as data sources
- To configure a different source, select either of the options and
  customize the connection

### Connection Information

- Create a data link file and browse to its location

## Advanced Settings

### Tables

- The fixed list of tables that
  Value
  Navigator looks for to complete a data update
- Required tables cannot be deselected

### Alias

- View/table name in the data source that corresponds to the Table name
- Defaults to PPDM 3.7 IHS or GeoLogic view names

### Query

- Optional text box to enter a custom query that generates the required
  columns from a proprietary data source

### Columns

- Columns and data types expected in each table/view available to select
  in a PPDM update
- Required fields cannot be deselected

To create views from a data source other than IHS or GeoLogic, create a
query that selects the expected columns from a data source and save it
in the Query text box in the dialog.
