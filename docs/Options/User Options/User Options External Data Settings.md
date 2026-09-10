



# User Options: External Data Settings

The PPDM Import options are used when you import production data. When
you update well production using IHS or GeoLogic data, a dialog box with
the PPDM Import options is displayed. You can change the options for the
current import, but the options will not be saved for the next import.
To change the import options permanently, edit them in the User Options.

## Data to Import

When importing data from an external source, only the selected data
types are imported.

## Monthly Import Options

### Import All Production History

Imports all production history.

### Import (number) Months of Production History

Selecting a number imports that number of months of production history,
going back in time from the
[Set the Current Month](../../Create%20Projects/Set%20the%20Current%20Month.md)

### Import All Available Production for New Wells

If enabled, this setting causes all production history for new wells to
be imported, regardless of the number selected for **Import (number)
Months of Production History.**

New wells are:

- Wells contained in a well list used during a PPDM import (see [Import Wells from a Well List (text file)](../../Importing%20and%20Exporting/Import%20Data/Import%20Wells%20from%20a%20Well%20List%20text%20file.md) )
- Wells in the project with no production history. If
  Value
  Navigator matches the UWI of a well in your project to a UWI in
  IHS or GeoLogic, it will import the well’s production history.

### Import Production History to End of (date)

Imports production history to the end of the specified date.

### Depths

This option controls the import of three depths simultaneously: GCI
Depth (gross completion interval), Measured Depth, and True Vertical
Depth.

- **Do not import**: Depths are not imported.
- **Import if missing**: Depths are only imported if they are missing.
- **Import always (overwrite)**: Depths are always imported and
  overwrite any existing depths in the project.

## Daily Import Options

### Import All Production History

Imports all production history.

### Import (number) Days of Production History

Selecting a number imports that number of days of production history,
going back in time from the
[Set the Current Month](../../Create%20Projects/Set%20the%20Current%20Month.md).

### Import All Available Production for New Wells

If enabled, this setting causes all production history for new wells to
be imported, regardless of the number selected for **Import (number)
Months of Production History.**

New wells are wells in the project with no production history. If
Value
Navigator matches the UWI of a well in your project to a UWI in
the imported data, it will import the well’s production history.

### Import Production History to End of (date)

Imports production history to the end of the specified date.
