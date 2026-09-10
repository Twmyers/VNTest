



# Set the Current Month

The current month is the month to which data is considered current. The
current month is displayed on **Wells and General Economics \| Well
Info** **and Custom Fields**.

The Set Current Month dialog box is displayed when you import data into
Value
Navigator only when the last production date found in the import
exceeds the
[Maximum Shut In Months If the number of months between the last production date and the Current Month exceeds the number entered in max Shut In Months, the wells are considered shut in. Shut-in wells are not auto-forecasted on import and do not receive an economic case when economics are run. By Default, shut-in wells do not receive data copied to them from the Economic Input Copier.](#)..

The current month is used to determine how current the production data
is, which enables
Value
Navigator to calculate if a well is shut in. For example, if a
production update is performed on June 2009 for 10 wells and 2 wells
have production history up to January,
Value
Navigator determines that the those 2 wells have not produced
since January. If the Max Shut In Months is set to less than 5 months,
the 2 wells are considered shut-in wells. Shut-in wells are not
auto-forecasted on import and do not receive an economic case when
economics are run. By Default, shut-in wells do not receive data copied
to them from the Input Copier.

The [User Options: Import Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md#Generate_Forecast_from_Last_Production_Month) setting affects
how the current month is set. If Forecast from Last Production Month is
enabled, the current month for wells that are not shut in is set to the
last production month. For shut in wells, the current month is set to
the last production month. If Forecast from Last Production Month is not
enabled, the current month is set to the last production month. See the
summary below.

| Forecast from Last Prod Month | Shut In? | Current Month is set to... |
|-------------------------------|----------|----------------------------|
| Enabled                       | Yes      | Most current date          |
| Enabled                       | No       | Last production month      |
| Not enabled                   | Yes      | Last production month      |
| Not enabled                   | No       | Last Production month      |

If you are creating a new project and want all wells to be
auto-forecasted, select **Generate Forecast from Last Production Month**
in [User Options: Import Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md) .

Also see [Set to Current](../Forecasting/Create%20and%20Edit%20Declines/Set%20to%20Current.md).

## How the Current Month is Set on New Entities

### PPDM

If a well is being created during an import or is loading data for the
first time from the PPDM, the Current Month is set to the provincial
current month found in the PPDM.

### File imports

If a well is being created during an import or is loading data for the
first time from a vendor flat file, the Current Month is set to the most
recent production date found in the file, unless it is more than 6
months old, in which case it will ask you to select a date to use for
Current Month.

## How the Current Month is Set on Existing Entities

### PPDM

When using Vendor PPDM data updates, the Current Month indicates the
date to which the data is current. The date can be different for each
province.

- **For producing entities**: The Last Production Month and Current
  Month are updated to reflect the most recent date and are usually the
  same.
- **For shut in or abandoned entities**: If a well stops producing and
  stops reporting, the Last Production Month set in
  Value
  Navigator is not updated. However, the Current Month is updated
  to reflect the provincial current month.

If a well stops producing but continues reporting production volumes as
zero, the Last Production Month and Current Month continue to progress
together and both are updated. Unfortunately, this can make it more
difficult to notice the well is shut in when the dates are current and
equal.

### File Imports

If a well is being updated from a vendor flat file, the Current Month is
set to the most recent production date found in the file, unless it is
more than 6 months old, in which case it will ask you to select a date
to use for Current Month.

- **For producing entities**: The Last Production Month and Current
  Month are updated to reflect the most recent date. The dates are
  usually be the same.
- **For shut in or abandoned entities**: If a well stops producing and
  stops reporting, the Last Production Month in
  Value
  Navigator is not updated, but the Current Month is still
  updated to reflect the current month from the file or as set by the
  user.

If a well stops producing but continues reporting production volumes as
zero, the Last Production Month and Current Month continue to progress
together and both are updated. Unfortunately this can make it more
difficult to notice the well is shut in when the dates are current and
equal.
