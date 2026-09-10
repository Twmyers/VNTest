



# Import Production Data Overview

To update production on the wells in your project you can use:

- A production data file you exported from a data vendor, such as
  Accumap (.vna) or GeoScout (.mer)
- A external data source (IHS or gDC)
- The [Import Spreadsheet Data Overview](../Importing%20and%20Exporting/Spreadsheet%20Import/Spreadsheet%20Import.md) (**.xlsx**,
  **.xlsm**, or **.csv** files)

The data can include:

- General Well Information
- Production History
- Pressure Data: Header Information, AOF Tests, BHP Tests
- Gas Analyses
- Working Interests
- Custom Data

You need administrator access to import data, to append data to existing
wells, or to load new wells into the project.

As production data is being imported,
Value
Navigator removes faulty data such as duplicate records and
pressure tests with no dates. An auto-forecast is generated from
production data for any new wells.

Before you update production, review the topics below.

## External Data Sources Connection Requirements

To update production using PPDM you need to have an:

- Oracle client installed
- IHS or GeoLogic subscription
- IHS or GeoLogic connection set up in User Options

To update monthly production using a corporate data hub, you need to
specify the **vnudl** file.

See [Configure an External Data Source](../Importing%20and%20Exporting/Import%20Data/Configure%20an%20External%20Data%20Connection.md).

## Configure External Data Settings

Before updating production you must configure the External Data Settings
in User Settings. See [User Options: External Data Settings](../Options/User%20Options/User%20Options%20External%20Data%20Settings.md) .

The External Data Settings control the type of data and the amount of
production history imported. You can configure these options before
updating production or during the production update. 

## Configure Import Parameters and Fit Settings

It is highly recommended that you review and understand the [Fit
Settings](../Options/User%20Options/User%20Options%20Forecast%20Settings.md)
and [Import
Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md)
in the User Options before importing production data. These settings
affect how data is imported and how forecasts are created in
Value
Navigator.

## Map Project UWIDs to the Data Source

The well names or UWIDs in your project must match the names or UWIDs in
the data source. Wells with names that do not match are not updated.

If the wells in your project were originally imported from the data
source you are using to update them, the names should match and you do
not need to map the UWIDs. However, the names or UWIDs might be
different if:

- You have used custom well names that a data vendor does not recognize.
  You can still use custom names, but you must map them to the names in
  the data source.
- The production data source you originally used to import the wells and
  the production data source you are now using come from different data
  vendors who use different names for the same wells

To determine if the well names are mapped correctly, see
[Map Data Vendor IDs](Map%20Data%20Vendor%20IDs.md).
