

# 2022 v2 Release Notes

## New Features

### BC Royalty Framework Updates

This release delivers the industry's most comprehensive model of the new
B.C. royalty framework that is aligned with evaluators for standardized
reserves evaluation in the province. With a sound and accurate economic
model, you can have confidence in the results so you can direct your
focus on the key economic drivers and analysis. Here is just a subset of
royalty aspects incorporated:

- The most up-to-date framework model including the new royalty rate
  price curves
- Production categories that smoothly handle the transition of existing
  and new wells between frameworks
- Proper handling of deep well credits, royalty reduction programs, and
  GCA based on category selection
- The ability to run the old royalty framework as-is to analyze the
  impacts of the new framework

### Bulk Operation Improvements

We’ve introduced significant improvements to the most popular bulk
operation tools, including Data Views, the Data Manager, production
updates, and spreadsheet imports. So, whether you are updating cost
inputs from the spreadsheet importer, changing well header information
from a Data View, or updating production history from an internal
production system, Val Nav will fly through the updates faster than ever
before. The improvements were made by drawing on learnings from the
economic engine, which includes multi-threading certain operations.
Similar to economics, options on thread allocation for these runs have
been introduced to the config file. Note that these changes are focused
on bulk operations only, so no performance changes are expected for
economic run times. The most notable operations affected are:

- Data View updates, including extra benefits to Well Info updates
- Production updates via an external data connection
- Spreadsheet imports including extra benefits to well info imports
- XML Imports
- All Data Manager operations
- Data Validator
- Recalc cached forecasts

### New BI-focused Views 

New BI-focused views will automatically be added to all Val Nav projects
upon upgrade, allowing deeper analysis and easy generation of management
presentations. The views blend key definitions and result streams in the
databases so that DBA knowledge isn’t required to extract meaningful
economic data. Simply connect your BI tool of choice to the
BTAX_CASH_FLOW view and start building.



### Multi-distribution Plotting

We added multi-distribution plotting. This enables you to split sample
sets into multiple probit plots or S-curves to analyze distributions
against each other. Build more accurate type curves by answering
questions like:

- How does well spacing or parent/child relationships impact the
  distribution profile?
- Are drill plans improving by vintage?
- Are some operators or completion styles outperforming others?



### Type Well Plotting Updates

The styling and functionality of the type well plotting have gotten a
few updates to improve the user experience and freshen up the UI:

- Type well decline can now be toggled on and off to see the final
  projection relative to analog wells
- You can now toggle between products and ratios
- A cumulative volume/time variant is now available
- Banding and gradients have been removed to provide more contrast
  (Insert picture attached)



### New Copy Multiple Tool

A new “Copy multiple” tool enables you to duplicate the current
selection of entities for a specified amount of iterations to solve
certain workflows, like duplicating a pad or grouping, downsizing
spacing requiring well count increases, and more.

## Other Enhancements

### Cross Plot Options Changes

The cross plot options have been cleaned up so you can focus on the most
relevant inputs for analysis. "Display UWI Labels" has moved to a
context menu for each plot, "Type" has been removed, and "View" has been
re-labeled to "Product"

### Expanded Clear Economics Functionality

We expanded the "Clear Economics" tool to enable more granular cleanup
of economic results by plans and scenarios. You must have the "Manage
database tables" or "Modify Project Options" privilege and will be able
to delete both project and user scenarios.

Other enhancements include:

- Made the following well attributes available to build a hierarchy:
  Status, Zone, License
- Added the ability to plot a cumulative vs time variant of the type
  well spaghetti plot.
- Added the ability to filter on "Spud Date" and "Is Grouped".
- Added a confirmation dialog to the "Clear all flags" button.
- Added the ability to overlay the type well decline on the type well
  spaghetti chart.
- Added the database name and path to the spreadsheet import log.
- Significantly improved performance of custom field updates from the
  Data Views and the spreadsheet import.
- Added a generic, unconfigured data source to External Connections in
  place of the FDC plug-in.
- Added Condensate to the "Daily History" report template.
- Added an "Apply ACCI to balance" flag on Alberta incentives to allow
  the exact balance, inclusive of ACCI, to be entered and used by the
  C\* calculation.
- Added "Kickoff" and "Landing" coordinates to allow more realistic well
  stick rendering on the map.
- Improved logging for CDW imports including notifications for longer
  than expected run times.
- Added menu options to control the axis plotting, sorting, and scaling
  of the S-curves found on the *Cross Plot \| Distribution* tab
- Reformatted the Distribution tab to give users more consistency and
  flow as they analyze data sets between Cross Plot tabs. The stats
  table has been moved in-line with the well info table allowing the
  distribution plot to be split into two plots.
- Cross plot options are now saved per user for all entity types except
  type wells and rollups, which offers more consistency as users analyze
  different data sets
- For plays where forecasts are derived by forecasting a liquid rate and
  water-based ratio, the forecasting engine has been updated so that a
  terminating WOR forecast terminates the entire forecast, matching
  existing 1+WOR and Oil Cut behavior. This equates to modeling a well
  watering out when too much water is produced relative to oil.
- Fiscal regimes available to add to an entity are now sorted in
  alphanumeric order.
- Changing the type well options now triggers a recalculation upon
  clicking OK.
- ARIES Converter: Added support for conversion of time-based ratios
  denoted by the TIME keyword
- ARIES Converter: Improved logging for improperly configured tables
  within ARIES databases.
- ARIES Converter: Improved logging and error handling when PROPNUMs
  referenced in AC_ECON do not exist in AC_PROPERTY
- ARIES Converter: Improved logging when columns in AC_PROPERTY are
  called via @M references but do not exist.
- Schedule Adjustment Plug-In: Fixed an issue where forecast start dates
  were not updated properly.
- Forecast Variance Plug-In: Improved the security model of the forecast
  variance plug-in for users with limited access to wells and global
  project data.

## Bug Fixes

Fixed issues where: 

- Certain entity types could not be exported from archives in SQL
  Server, including type wells.
- Duplicate meter stations were created upon project creation.
- Cost entities would incorrectly terminate based on fixed op cost
  termination.
- Royalty calculation of plant condensate would fail with inactive
  company.
- O+W and WOR were incorrectly interpreted as a product conflict.
- The "Cum. to end" volume would incorrectly calculate if a mid-month
  forecast start date overlapped with production history.
- Upgrades could fail when rollups are present.
- An entity rescat forecast would be generated when re-applying a type
  well link.
- The "Reserves Categories to Balance" and "Disclose" Reserves groups
  were not sorted by their specified order.
- The reconciliation of the "Regimes/Royalties" input area could
  calculate incorrectly.
- The "Apply Normalization" field was not sorted alphabetically.
- Vendor IDs could crash if the FDC plug-in was not installed after
  previously being added.
- The command line import does not use app.config log settings.
- The wrong reserves category could show in the "Common Termination"
  report
- The copy entity dialog position is not remembered.
- A recalculation of normalized type wells would trigger upon entering
  the Type Well tab.
- The type well graph would flicker when selecting different child
  wells.
- The Save icon was enabled when entering the Interests & Royalties tab
  just after upgrade.
- The "Per Plan" option in the Scenarios dialog would overlap the rest
  of the options when enabled.
- Fixed an issue where temp DrillingInfo files would not be deleted
  after import.
- The timing of ratio segments was not properly converted in the ARIES
  Converter.
- Certain cost timing was only correctly converted in the PDP reserves
  category in the ARIES Converter.
- Certain Abandonment and Salvage keywords were improperly handled in
  the ARIES Converter.
