# Val Nav 2023 v2 Release Notes

## New Features

- The Forecast Variance workflow incorporated in Val Nav 2023 also sees
  an update in usability. Now, the calculation can use the forecast
  backfit so variance can be run at any time. Simply, run the variance
  from the Forecast menu at any time and find the wells deviating most
  from production to focus your efforts on!\
  \[Id: 237629\]

- Single-well and AFE economics is often about normalizing timing for
  comparison against time-sensitive economic indicators like NPVs and
  RORs. For instance, analysis of two identical wells drilled in
  February and December would favor the February well if the basis of
  comparison was the NPV as of January since more discounting is
  required for the December well.

  To help with this challenge, the reference and discount dates can now
  be set for individual wells. With a well-level reference and discount
  date placed at first spend, AFEs can be compared on a fair, equal
  footing. Note that this functionality is best suited for single-well
  economics, so shared calculations like CTEs, Ring Fences, and
  folder-level results will continue to use scenario or project
  reference dates. \[Id: 147822\]

- \
  Economic modeling leaps forward again in Val Nav 2023 v2, extending
  the lookup model to operating costs. Just like capital costs, they can
  now be templated as lookup models that are assigned for wells to
  reference.\
  Sharing the same structure as price decks, opex decks with lookups
  automatically update all wells that use them. Sensitivities can be
  created just by running different decks without any change to the
  wells.\
  Even better, they are built relative to an anchor date on the well so
  costs are scheduled dynamically. As each well's schedule evolves, Val
  Nav updates the cost timing based on the updated anchor date requiring
  no extra updates from the user.

  Altogether this means that cost modeling will be more efficient,
  trusted, and connected than ever before. \[Id: 228382\]

- Continuing our story of performance improvements across recent
  releases, we’ve introduced significant performance improvements to two
  of the most critical workflows: calculating economics and moving
  between entities. Both see boosts from a variety of optimizations
  including one larger change for each:
  - Economic result cleanup will now be run asynchronously from the
    calculation for SQL and Oracle-based projects. This removes a key
    bottleneck from the calculation process.
    The cleanup method will be controllable by the application config
    file and can be reset to current behavior.
  - When selecting a well, only the data from the selected tab will be
    loaded, boosting performance by minimizing data requests.

  Altogether, Val Nav will fly through calculations and users will glide
  between wells faster than ever before!\
  \[Id: 232765\]

- \
  \
  With an increasing focus in the industry on near-term forecasts, Val
  Nav 2023 v2 introduces functionality to model the impact of
  operational events like tubing replacements, re-fracs, plant
  turnarounds, and much more on the long-term forecast. Doing so in the
  same platform that generates your long-term forecasts simplifies your
  workflow, saves valuable time and effort, and reduces the risk from
  data translation and transfer. This precision allows you to
  confidently predict pipeline commitments and monthly outlooks.

  With the new short-term production modeling functionality, you will be
  able to:

  - Define operational event types at a project level.
  - Configure whether operational events preserve or factor volumes.
  - Enter daily per-product factors to model the effect of the event and
    refine the long-term well forecast.
  - View the impact of the events on the Wellhead tab.
  - Bulk update well-level events with standard tooling: Data Views,
    Spreadsheet Import, Input Copier, and more.
  - Store the volumes lost, created, or deferred from these events in
    the database for analysis.

  \[Id: 228369\]

- \
  \
  Val Nav 2023 v2 also adds thoughtful improvements to type curves with
  a focus on how they are applied to undeveloped wells in Asset or
  Reserves projects:\
  - A new spreadsheet import for type curve links is available so
    undeveloped wells can be updated en-masse, including dynamically
    determining the scaling factor via our three scaling modes: Existing
    Factor, Production, and Normalization.
  - When sharing type curves between databases, an option to exclude
    analog wells has been added so that only the type curve parameters
    are sent. This improves sharing to Asset and Reserves databases that
    typically don't have all of the competitor analog wells in the
    dataset.

  \[Id: 239634\]

## Enhancements

- Added the following events to track in project history: plan
  modifications and company additions, deletions, and modifications.
  \[Id: 227838\]
- Added the entity object ID as read-only to the data view to improve
  the process of working in databases, BI tools, and archives. \[Id:
  235681\]
- Added a new anchor option for costs that may be independent of entity
  timing, a lookup can now anchor to a fixed date: "Manual Date". \[Id:
  236084\]
- Added a new operating cost to model transportation costs that apply to
  the net lease produce volume: "Net Variable GP&T Cost". \[Id: 232589\]
- Added graph comments to view on the Comments tab. \[Id: 132591\]
- Extended the number of available daily pressure fields from 10 to 20.
  \[Id: 100327\]
- Added more zoom options for previewing Reports. \[Id: 244608\]
- Improved handling of very steep declines that calculate secant and
  tangent declines that are too large to store in a database. \[Id:
  160020\]
- Added an option to calculate forecast variance using calendar day
  rates. \[Id: 241084\]
- Clarified hierarchy and scenario visibility options in their dialogs.
  \[Id: 245599\]
- Standardized usage of the Well Status field that was inconsistently
  referred to as "Status" or "Well Status". \[Id: 174938\]
- Allowed "Well Name" to be used as the Asset Name on the export to
  Enersight. \[Id: 245710\]
- Introduced the ability to bring back Enersight's calculated producing
  time back into Operational Events. \[Id: 240862\]
- Removed padding on API numbers to store 14 digits so exact lengths can
  be stored. \[Id: 90963\]
- Added in-app warnings when fits are requested but aren't generated due
  to a variety of reasons including invalid user options, wells deemed
  to be shut-in, and more. \[Id: 239506\]
- Introduced a new dynamic product mapper to the Import from Enersight
  to support unique workflows in Enersight. \[Id: 244667\]
- Made daily pressure fields optional in data source imports. \[Id:
  241869\]
- A new Data Manager tool has been built to convert lookup costs into
  manual costs: "Realize Lookups". In a few use cases, wells using
  lookups need to be disconnected from the live lookup and realize them
  as manual inputs on the well: ◦To capture the assumptions of an AFE
  made at the time of approval. ◦As an undeveloped entity approaches
  development and cost assumptions need to be further refined than the
  generic lookup model. ◦For use by the Val Nav-Execute integration to
  populate projects in Execute’s Budgeting and Forecasting module. \[Id:
  239627\]
- We’ve introduced more flexibility to deal with the different
  variations in how API numbers are stored and reported elsewhere. Now,
  you can import by proxy against API-10, -12, and -14 whether formatted
  with dashes or not, and you can view the unformatted version in the
  data view alongside the formatted one. \[Id: 124430\]
- Removed limitations on the discount date that required it be set
  before the reference and economic calculation start dates. \[Id:
  242569\]
- Redesigned archive modes to simplify options and introduced an
  economic-input-only mode to reduce archive sizes when full economic
  results are not necessary. \[Id: 229982\]
- Updated the branding across the app. \[Id: 244666\]

## Fixed Defects

- Fixed an issue that caused the Technical Comparison tab to crash
  occasionally. \[Id: 248134\]
- Fixed an issue where changes to the Ops Event data area would not
  trigger when editing Common through from another reserves category.
  \[Id: 235650\]
- Fixed an issue where custom result fields were not imported via XML.
  \[Id: 236196\]
- Added optional logging for issues related to multi-threaded
  operations. \[Id: 236082\]
- Improved error messages related to invalid production categories in
  the economic services log. \[Id: 178670\]
- Fixed an issue where the New Mexico Emergency School Tax Oil Rate was
  incorrectly set at .0315% instead of 3.15%. \[Id: 105542\]
- Fixed an issue where graph scaling was reset when changing decline
  parameters. \[Id: 248148\]
- Updated the Hotkey legend to reflect the rename of the "B"-factor arps
  parameter from "N". \[Id: 244771\]
- Fixed an issue where the Arizona Privilege Tax Rate was incorrectly
  reset in June 2010. \[Id: 150208\]
- Fixed an issue where certain Oracle character configurations could
  disallow custom currencies. \[Id: 228073\]
- Fixed an issue where lease start and end dates were ignored in custom
  fiscal regimes. \[Id: 244416\]
- Fixed an issue where cases would require recalculation upon opening a
  project when capital cost decks were not used. \[Id: 250662\]
- Fixed an issue where the Choke Size daily field would not plot on
  custom graphs. \[Id: 241404\]
- Fixed an issue when using "Draw Profile" where short, flat segments
  would not be created properly. \[Id: 241965\]
- Fixed an issue where technical gross ultimate volumes could be
  double-counted on certain reports. \[Id: 234722\]
- Fixed an issue where PCOS deductions were improperly calculated when
  using new BC royalty production categories on wells with multi-product
  interests. \[Id: 244349\]
- Fixed an issue where an error is triggered by opening the Print
  Preview from the Report Designer on a report that does not have any
  entities selected. \[Id: 175766\]
- Fixed an issue where Monthly/Annual tables show "Jan 0001" for dates
  with no entry. \[Id: 175768\]
- Fixed an issue where y-axis max/min settings are occasionally not
  maintained while switching between wells. \[Id: 241204\]
- Fixed an issue where Sandbox entries on General Economics do not show
  in Data View. \[Id: 164383\]
- Fixed an issue where non-line series styles do not show up on the
  Technical Comparison tab. \[Id: 249816\]
- Fixed an issue where the plant tab of type wells could not be opened
  if their plant data was changed in the data view. \[Id: 237984\]
- Upgraded map components to address a newly discovered Chromium
  vulnerability: CVE-2023-4863. \[Id: 247691\]
- Added "Zone" to the list of reserved names so duplicates can be
  created. \[Id: 244946\]
- Fixed an issue where clicking away from and back to a well while in
  fit mode would cause a crash. \[Id: 242780\]
- Fixed an issue where the waterfall chart would not respect the current
  unit system. \[Id: 246265\]
