

# 2024 v2 Release Notes

## New Features

### Import Price and Cost Decks from Excel



Building on our transformative lookup story, Val Nav 2024 v2 introduces
the ability to import price and cost decks directly from Excel, saving
time managing cost lookups, stream price projections, and other fiscal
data like taxes, royalty prices, and inflation!

Updates start with a direct-to-Excel export of your current data, so you
can easily review and validate all assumptions in Excel first, ensuring
accuracy and consistency with a look & feel you are familiar with. Once
you are ready to import, Val Nav will validate the data to ensure its
integrity, allowing you to make direct Excel edits to address any
warnings.

See [Import Global Project Data](../Importing%20and%20Exporting/Import%20Data/Import%20Global%20Project%20Data.md) for more information.



Remember: All global project updates, including price and cost deck
imports, should be made in a locked project with no other users in the
system.



### Advanced Insight Generation



Val Nav 2024 v2 advances its leading insight generation with
improvements to both the technical comparison and the cross plot tabs:

- Plot daily actuals in the technical comparison tab for a more detailed
  comparison of history and forecasts.
- Build comparisons more intuitively in the Technical Comparison tab
  with:
  - Modes re-imagined as quick-add starting points rather than strictly
    enforced comparison views.
  - A UWI option to either pin the explicit entity or the "Current
    Entity" while honoring the other dimensions: Plan, Res Cat, and
    Archive.
- Control which axes and regions in the Cross Plot tabs are normalized
  to accommodate comparison across datasets that already are or
  shouldn't be normalized.

### Royalty Updates

We have also updated the new British Columbia royalty framework with the
latest information from the provincial BC government, reflecting:

- The new date to transition to the new framework: January 2027.
- The Producing Hours incentive's dependency on well type.
- The extension of the Deep Well Deductions life to September 2027 for
  existing wells.

Like our previous release, these framework inputs can be changed via a
custom fiscal regime available on request. This regime, which does not
need to be added to wells, was also simplified for more intuitive
updates.

Check with our support team for more documentation on these updates and
associated fixes.

### Enersight Integration

We've enhanced the Enersight integration to improve reliability in the
full cycle integration story and accommodate market-specific use cases
like Canadian royalty handling across both tools:

- Enabled the integration to send BC and Alberta royalty details
  including BC\* and C\* remaining balances and effective dates
- Added filters to the opportunity table on the import back from
  Enersight for easier opportunity selection.
- Amended the mapping approach between Enersight production sets and Val
  Nav for clearer and more reliable reserves category matching when
  importing.

## Enhancements

- Renamed the PCOS 2024 field, which acts as the stand-in for GPA
  calculations as we await details from the BC government, to GPA,
  removing mention of the outdated 2024 transition.
- Removed plan-level headers from custom report template that filtered
  history results from wells without entries in those fields.
- Simplified the custom BC Royalty Framework regime that allows users to
  update key inputs like the transition date, in anticipation for
  further changes to the framework and its timing. Note: This regime,
  which can be requested from support, does not need to be added to
  wells.
- Renamed the Forecasts Data View to avoid internal conflict automating
  tests.

## Fixed Defects

- Fixed an issue where certain decline builds requiring iteration would
  not solve within the max iteration count by increasing the limit.
- Fixed an issue where the left border of the Economics \| General tab
  was cut off.
- Fixed an issue where economic results for BC wells were not viewed as
  stale when spud date had been changed.
- Fixed an issue where attempting to change units in the Cross Plot tab
  grids caused an exception.
- Fixed an issue where fiscal regime variables incorrectly started
  calculation from the reference date instead of the economic
  calculation start date.
- Fixed an issue where a particular well in a .vna import would not
  match to its equivalent UWI in Val Nav causing it to be duplicated.
- Fixed an issue where entity locks were not release after performing a
  bulk operation from the data view.
- Fixed an issue where unites of Op Costs in lookups were not
  remembered.
- Fixed an issue where manual on-time could end prematurely end a
  partial month end date.
- Fixed an issue where Volume-slope ratios would occasionally not be
  solved when the ratios and independent product are anchored.
- Fixed an issue where the Set Start of Forecast would incorrectly
  unanchor some declines that progressed past their initial anhored
  segment.
- Fixed an issue where date adjustment tools would keep unwanted
  hour-minute granularity added from tools like Excel. Now, these tools
  will only use day-level granularity. Note: Decline calculations are
  still instantaneous.
- Fixed an issue where inline text values in Excel are not recognized in
  Val Nav's spreadsheet import.
- Fixed an issue where selecting a deleted entity while on the Timeline
  tab would cause a crash.
- Fixed an issue where list item colours could not be edited on the map.
- Fixed an issue where lateral length would not recalculate with updated
  lat/long coordinates.
