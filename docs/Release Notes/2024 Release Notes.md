

# 2024 Release Notes

## New Features

### A New Paradigm for Scheduling

Val Nav 2024 introduces a brand-new approach to scheduling that will
make re-scheduling your wells and analyzing development decisions a
breeze.

We have extended lookups to dynamically schedule against new well-level
Activity Dates meant to mirror real-life activities. This separates
assumptions on unit costs and decline parameters from timing allowing
simpler discrete modeling updates, which more closely aligns with how
engineers receive and make updates.

Explore all the new possibilities:

- Run and compare different scheduling scenarios with ease.
- Quantify the impact of schedule changes with automated reconciliation.
- Update entire asset schedules from field development planning tools
  like Enersight or your favourite spreadsheet.

### Anchored Forecasts



 

Critical to this improved scheduling is the ability to anchor decline
start dates to Activity Dates. You can now shift forecast timing across
products and reserves categories with ease and precision from a single
Activity Date! While quicker to update with new assumptions and
sensitize timing for analysis, it also makes wells more transparent for
simpler auditing.

We’ve also accompanied the start date changes with a few alterations to
segment parameters:

- Anchor offsets can stagger a decline start from the activity date –
  for instance, to aid in modeling water breakthrough in waterflood
  projects.
- Segment duration is now a distinct input, offering a better
  rescheduling experience where segments float through time with
  constant duration.
- End dates can still be used to account for fixed-in-time segment
  terminations.

### Improved Reforecasting with Anchored Forecasts



Another major benefit of Val Nav’s new approach to scheduling is tied to
fitting producing wells. Now, when reforecasting any anchored decline,
all others dependent on the same anchor date are interpolated or “walked
down” to reflect the new timing while honouring their curve shape and
EUR.

Now you can focus solely on products in need of updates while Val Nav
keeps all other declines in lockstep, simplifying QA/QC and secondary
product updates.

### Custom Data Validator Rules

Build confidence in your asset and reserves plans with the latest
addition to the Data Validator. In Val Nav 2024, you can build your own
validation rules leveraging filters and share them globally across the
organization, empowering teams to ensure completeness and accuracy in
their assumptions. Build rules that validate whether:

- Producing wells in certain formations have b-factors in a
  corporate-approved range.
- Undeveloped wells have the proper lookups assigned based on a custom
  field input.
- Ensure all required fields have entries so they are properly included
  in aggregations.

And much more!

### Colour Well Sticks



A customer favorite just got another update: you can now colour the well
sticks on the map separately from the bubbles to add another dimension
to your spatial analysis! Whether examining the classification of offset
wells or colour-coding sticks by formation in a stacked play, the added
visual helps drive further insights in plays across the world.

### Royalty Updates

With uncertainty still surrounding aspects of the new British Columbia
royalty framework, we have built more flexibility into certain framework
inputs. Through a custom fiscal regime available on request, you can
update assumptions in the framework like when the transition to the new
framework will happen, when deep well deductions will terminate, and
more.

We’ve also updated the Saskatchewan royalty framework to accommodate two
new programs:

- Saskatchewan High Water Cut Program
- Saskatchewan Multi-Lateral Drilling Incentive

Check with our support team for more documentation on these updates.

### Enhancements

- Refactored the implementation of volume-preserving ops events to:
  - Ensure forecast accuracy is insensitive to how segments are
    constructed.
  - See the impacts of volume-preserving ops events on the graphs in the
    Decline tab.
  - See the impacts of both non-volume-preserving and volume-preserving
    ops events on the Daily Forecast report.
  - Note: The impacts of non-volume-preserving events are still not
    visible on the graphs on the Decline tab.
  - Note: While volume-preserving are entered on a daily granularity,
    they impact the Daily Forecast report by applying the monthly
    average On-Time across the entire month.
- Added both forecast anchor and anchor date inputs to the decline
  toolbar for quick schedule updates directly from the tab.
- Updated the Active Directory integration to view all users within a
  nested AD group.
- Updated Draw Profile to create duration-terminated segments, aligning
  with the new best practice approach to segment creation.
- Updated segments to hide calculated parameters dependent on segment
  errors to provide a stronger indication of error and reduce confusion
  from improperly displayed calculations.
- Updated segment creation tools with logic to determine whether to
  create start dates anchored or user-entered. When not overwriting a
  pre-existing segment, Val Nav will default to creating anchored start
  dates; otherwise, it will attempt to honour the method used in the
  pre-existing segment.
- Updated Apply Type Curve logic to:
  - Honour the start date style on the destination well
  - Default to anchored start dates when the destination well has no
    forecast.
  - Offer the user the option to override the forecast anchor and/or
    activity date pending the method used.
- Added Activity Dates as variables in the fiscal regime engine for
  dynamic, date-based fiscal calculations.
- Updated Project Start to move activity dates, following the same
  behavior it uses to shift capital.
- Updated the Bulk Well Generator to both use source wells and generate
  wells utilizing activity dates.
- Added an option within the Realize Lookups dialog to un-anchor
  forecasts, which will revert the start date to user-entered at the
  date it was inheriting and remove the forecast anchor.
- Enabled the Set Start of Forecast tool to update activity dates and
  all forecasts dependent on the activity date. Updated the Set Start of
  Forecast tool's logic to extrapolate or interpolate when updating
  forecasts before the end of history and transposing them after it.
- Updated Set Start of Forecast to unanchor groups when called via a
  production import.
- Updated Snap to Current to unanchor forecasts.
- Deprecated the Forecast Start anchor from lookups to enforce the
  Schedule data area as the only data area that can adjust others'
  timing. On upgrade, lookups using this anchor will be replaced with
  the default activity date anchor, which will be populated with the
  forecast start date.
- Enhanced the Active Directory integration to be more resilient to
  improperly configured AD accounts.
- Added an option to the batch manager to skip print preview and export
  direct to destination files, which saves significant time if in-app
  rendering of results is not necessary.
- Users with the "Edit Global Project Data" policy can now create and
  edit new global filters that all users can see and use.
- Updated the capital plot on the Bulk Well Generator definition tab to
  reflect capital from lookups.
- Updated .VNA file imports to recognize Enverus' rebranding of
  DrillingInfo files.
- Updated the capital plot on the timeline tab to reflect capital from
  lookups.
- Updated the Bulk Well Generator to disallow changing the capital
  factor when the source well uses lookups for capital cost.
- Updated the "Total Reserves and NPV" report to disallow currency
  selection since one-line reports cannot support multi-currency
  reporting.
- Updated the Hotkey legend to reflect the rename of the "B"-factor arps
  parameter from "N".
- Added additional logging on exceptions stemming from
  **DataSetOperations** methods.
- Added the Input Copier to the context menu shown when right-clicking
  an entity in the hierarchy.
- Updated the messaging shown when upgrading a project from an earlier
  version for clarity.
- On close, Val Nav will store the user's last entity if either a Well
  or Group and re-open to this entity using the active hierarchy on
  project open.
- Added logging of deleted entities to the audit trail. Added a project
  option that when enabled keeps Deleted Entity records of deleted
  non-reserves entities.
- Improved logging of failed fitting routines.
- Improved security of XML Imports.
- Re-organized Entity tabs to re-enforce encouraged Entity workflow and
  reduced clicks, including: - Upgraded the Plant tab to a standalone
  tab within the Forecasts major tab. - Migrated the Gas Analysis tab to
  be a minor tab within the Plant tab. - Upgraded the Price, Operating
  Cost, and Capital Cost tabs to standalone tabs within the Economics
  major tab. - Renamed the Review tab to the Reconciliation tab.

### Fixed Defects

- Fixed an issue where Forecast Variance custom fields would not show in
  the hierarchy editor on creation until the project was closed
- Fixed an issue where the filter dialog would not re-open to the
  applied, saved filter.
- Fixed an issue where the auto-reconciliation would stall when run from
  a folder that included wells with multiple jurisdictions.
- Fixed an issue where type well segment values could not be updated
  from the data view.
- Fixed an issue where the "Copy to" command would not honour the
  normalization setting of the source type well.
- Fixed an issue where the Technical Comparison tab incorrectly allowed
  the selection of calculated plans.
- Fixed an issue where Draw Profile mode would not generate a profile on
  clicking Apply.
- Fixed an issue where the summary panel would not reflect the correct
  inputs and calculation state in archives.
- Fixed an issue where the Entity Summary tab would not show all rescats
  with input.
- Fixed an issue where Val Nav could crash when opening an archive with
  limited custom-field-based view permissions.
- Fixed an issue where a fit was found but still produced an error.
- Fixed an issue where the Draw Decline tool could throw an exception
  when run from the Workspace tab.
- Fixed an issue where filtering to selection could fail.
- Fixed an issue where the recently introduced GP&T Op Cost was
  incorrectly interpreted as a revenue based on gross volumes rather
  than a cost based on net volumes.
- Fixed an issue where wedges would not use calculation options like
  whether to enforce the economic limit from an associated total causing
  some wedges to incorrectly be deemed negative wedges, which could be
  disallowed by the project options.
- Fixed an issue where the Set Start of Forecast would extrapolate or
  interpolate a volume-based ratio with minor inaccuracy.
- Fixed an issue where the recently introduced Lost Volumes would
  incorrectly calculate in a variety of circumstances.
- Fixed an issue where the map's context menu would not appear when
  right-clicking the map.
- Fixed an issue where the map could no longer be panned after zooming
  in with the Control button.
- Fixed an issue where shared calculations could fail with the message
  "Max expected Iteration Count reached" despite a valid termination
  date being found.
- Fixed an issue where a well's resolved operating cost values would not
  reflect necessary currency conversions in the UI.
- Fixed an issue where Val Nav would not retain customizations made to
  the Operational Events data view.
- Fixed an issue where well count would start when plant ratio or
  efficiency inputs were entered without wellhead production.
- Fixed an issue where recurring operational event values were ignored,
  causing incorrect forecast results.
- Fixed an issue where Val Nav could crash in the Report Designer when
  clicking on the grid in the edit tab.
- Fixed an issue where telemetry data was unclear due to identical tab
  names.
- Fixed an issue where the Remaining Equivalent Reserves section in
  Total Reserves reports would not reflect the user's unit system
  setting.
- Fixed an issue where the entity hierarchy would lose focus disallowing
  users from scrolling between entities with up/down arrows.
- Fixed an issue where users could not delete liquid ratio arrays from
  the Plant tab.
- Fixed an issue where plant data would re-appear after being deleted
  from the Plant tab data view.
- Fixed an issue where Val Nav would crash when two hierarchies match
  exactly except for a case mismatch and entities are merged between
  them.
- Fixed an issue where incorrect volume-preserving ops events could be
  used when calculating the total with wedge inputs.
