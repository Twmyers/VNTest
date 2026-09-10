

# 2019 Release Notes

## What's New

### Password Requirements Change



If your password contains non-ASCII characters, you must change it to
contain only ASCII characters before you upgrade a project to
Value
Navigator 2019. If you upgrade a project without updating your
password to contain only ASCII characters, you'll be locked out of the
project.



Value
Navigator 2019 contains security changes to its password-hashing
algorithm. Previously, we were hashing all passwords as ASCII text, but
now are hashing with a UTF-8 algorithm. This means that the password
hashes for non-ASCII characters (accented letters, Cyrillic characters,
etc.) have changed, and those passwords will not be validated in
upgraded databases.



Active Directory (single sign-on) users are not affected.



[Read more here.](../Getting%20Started%20with%20Value%20Navigator/ValNav%202019%20Password%20Requirements.md)

### Daily Data Forecasting

Value
Navigator 2019 is focused on daily data forecasting. We've added
a variety of new features to help you get better use of your daily data:

- Fitting: do auto-fits on your daily data
- Graph interactions: daily-data versions of fit-from-point and
  fit-from-selection
- Daily data comments on graphs: if your daily data has comments, you
  can now render them on graphs
- Misc. graph improvements: added daily series to our default graphs,
  new daily-specific graphs, improved daily data point rendering, and
  more

See [Best Fit Daily Data from a Point or a Selection](../Forecasting/Create%20and%20Edit%20Declines/Best%20Fit%20Daily%20Data%20from%20a%20Point%20or%20a%20Selection.md)
and [Display Daily Data Comments on Graphs](../Graphing/Use%20Graphs/Display%20Daily%20Data%20Comments%20on%20Graphs.md).

### Quick Graph Scaling

Quickly rescale your decline graphs with the following shortcuts:

- Double-click: Set axis maximum scale
- Shift-double-click: Set axis minimum scale
- Middle-click: Reset scaling on single axis
- Shift-Z: Reset all quick scaling



 

See [Customize Graph Scaling](../Graphing/Use%20Graphs/Customize%20Graph%20Scaling.md).

### Control Graph Log Cycles

We’ve added a new option on graphs, to fix the number of log cycles for
all axes within a region. This allows for more consistent data display,
particularly when combined with the quick graph scaling above.



See
[Control Graph Log Cycles](../Graphing/Use%20Graphs/Control%20Graph%20Log%20Cycles.md).

### Rename Reserves Categories

You can now provide your own custom names for our built-in reserves
categories.



With the ability to rename reserves categories, the reserves category
names formerly stored in the CODE_LOOKUP table are no longer used, and
those rows will be deleted on upgrade. Queries referencing the
RESERVE_CATEGORY code type in that table will need to be rewritten to
instead join on the FISC_RESERVE_CATEGORY table.





See [Rename Reserves Categories](../Entity%20Management/Rename%20Reserves%20Categories.md).

### Producing-Time Graph Axis

We’ve added a new graph x-axis for producing time, available in our
graph designer. This helps strip out downtime to help you better see
trends.



### Mass-Based Oil Forecasting

We have introduced a new Oil (Mass) product and product list, for
forecasting oil in mass units (e.g., tonnes/d), with a well-level oil
density for automatic conversions between the two. You can have
mixed-unit mass-based and volume-based forecasts on the same well,
including fluid forecasts (O+W and 1+WOR).

The focus on mass-based oil forecasting for VN 2019 was on the technical
side, so we recommend using caution when extending use to economics and
reserves -- there are some known limitations around reporting at this
time.



See [Add a Product to an Entity](../Entity%20Management/Products/Add%20a%20Product%20to%20an%20Entity.md).

### Drilling Info Import

See [Add a Product to an Entity](../Entity%20Management/Products/Add%20a%20Product%20to%20an%20Entity.md). See Add a [Product to an Entity](https://documentation.aucerna.app/valnav/2019/Entity%20Management/Products/Add%20a%20Product%20to%20an%20Entity.htm?Highlight=add%20a%20product).

### Drilling Info Import

We now support importing wells and production data from DrillingInfo
.dri files.



### Report Designer Enhancements

The Report Designer has been updated in a variety of ways:

- Additional gross and net fields
- Include user-built reports in the Templates list
- New functions: Join, First, ValueAt
- New economic indicators for discounted payout
- New US-style cash flow and one-liner reports



### Tax Updates

Value
Navigator’s US and Canadian tax calculations have been updated to
support recent legislative changes.



## Schema Changes

See schema changes
[here](../Schema%20Changes/VN%202019%20schema%20diagram.pdf).

## Fixes

### Forecasting

- Updated the XML format to include fractional-daytime components in
  decline segments. This would cause exported wells to have different
  reserves after importing, because segment transitions would occur at
  slightly different durations. This resolves a known issue from 2017
  v2.
- Fixed an issue in the decline calculation for Max Rate-limited
  forecasts, where primary product results could be incorrect if a
  volume-slope's secondary ratio was also modeled on the case.
  Additionally, an issue where on-time was not correctly taken into
  account when applying a Max Rate was fixed.
- Fixed potential infinite loop problem in the forecast calculation
  logic.
- Added the Sandbox plan to the Apply/Remove Type Curve dialog.
- Fixed an issue where the Forecast Mode was not copying to the Sandbox.

### Economics

- Fixed an issue where the use of a price factor in a scenario could
  cause a calculation failure
- Fixed an issue with common termination entities, where a cost entity
  could carry fixed operating costs to the abandonment date instead of
  to the economic limit.
- Fixed an issue where Tangible tax pools would not depreciate. The
  pools are now treated as beginning in year two of the MACRS schedule
  and depreciate from there.

### Reporting

- Fixed an issue in the Report Designer where the *Show Uneconomic
  Entities* option would not always work.
  *Show Uneconomic Entities*
- Fixed an issue in the Report Designer where the *Show Uneconomic
  Entities* option would not always work.
- Fixed an issue where some gas reserves product types would not show
  raw values in the Report Designer and Custom Reporter.
- Fixed an issue where a manual GOR of 0.0 could result in a well count
  being generated, which would then result in unwanted \$/well/mo fixed
  op costs being calculated. The well count is now correctly left at 0
  also.
- Fixed an issue where the calculation would end early on cases that
  terminate between the Economic Calculation Start Date and the
  Reference Date. This caused incorrect lower current-period reserves,
  but still correctly reported zero remaining reserves.
- Fixed an issue with the calculation of the probable and possible
  wedges where certain combinations would inadvertently clear prior
  calculated results, resulting in a well needing to be recalculated
  unnecessarily.
- Fixed a crash on the Reports tab.

### Reserves Management

- Fixed the 'Show oil and gas details' option on the Change Record
  Summary and Reserves Reconciliation reports. Previously, it was
  reversed, where having the box selected would hide the details instead
  of showing them.

### Graphing

- Fixed an issue where the Forecast Start and Reference Date lines could
  be misaligned between different regions on rate/cum plots.
- Updated graphs to remove collision detection for point graph series.
  This will prevent points from being hidden when they are close
  together.
- Fixed an issue where x-axis lines would only be shown on the bottom
  region of a multi-region decline graph.
- Fixed an issue where secure custom fields could be edited by a user
  without appropriate permissions.

### Miscellaneous

- Fixed an issue where incorrect warnings about being unable to resolved
  prices were logged.
- Fixed an issue where using Cyrillic and other Unicode characters could
  cause wells and/or folders to disappear from the entity hierarchy.
- Fixed some issues in .csv file handling for regions where the list
  separator is not a comma.
- Fixed an issue where calculation errors could cause the calculation to
  run indefinitely instead of terminating where the error was
  encountered.
- Fixed an issue where type well links were not being merged to new
  plans.
- Fixed an issue where having a CDW/PPDM plug-in installed on an earlier
  version could cause a crash on newer versions without that plug-in
  installed.
- Fixed an issue where valid 298c files would be rejected as invalid.
- Fixed an issue on the spreadsheet import using regional settings where
  the decimal separator was a comma. Will now handle all regional
  settings correctly in these imports.
- Fixed an issue on the Timeline tab that could cause a crash when wells
  had no capital.
- Fixed a crash that could occur when enabling Active Directory
  integration for security.
- Added logging when attempting to open a corrupt .vndb file.
- Fixed crashes that could occur using costs with long names.
- Fixed an issue where certain XML imports could cause a crash.
- Fixed an issue where new Saskatchewan condensate wells would not have
  the correct default production category assigned and thus no
  royalties.
- Fixed an issue that could cause a crash if an XML import was performed
  while on the Waterfall tab.
- Fixed an issue where the TPP \&gt; PDP category transfer was not working
  correctly.
- Fixed an issue where the production update progress dialog could be
  hidden behind the main
  Value
  Navigator window.
- Fixed a script warning issue on the What's New dialog when no internet
  connection was available.
