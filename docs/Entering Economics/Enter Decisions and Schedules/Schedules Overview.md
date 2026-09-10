

# Schedules Overview

The Schedules feature helps teams model how timing influences economic
evaluations. It introduces a structured way to define development
timelines using Activity Dates and apply those timelines across the well
inventory to control when production and costs occur.

By using Schedules, evaluators can:

- Represent the timing of development activities in a consistent,
  reusable way
- Tie the timing of economic inputs to when wells are planned to be
  drilled, completed, and brought online
- Rapidly update timing assumptions across the inventory by shifting
  well-level Activity Dates

For example, a well’s *Planned Spud* and *On Production* dates can drive
when drilling costs, operating expenses, and production forecasts occur.
Together, these Activity Dates define a well’s place on the development
timeline and enable robust schedule-based planning.

## Timing through Lookups & Forecasts

The Schedules feature aligns well-level timelines to cost and production
models in different ways.

For capital and operating costs, individual costs within lookups are
input relative to specific Activity Dates. Wells then have their own
values for these Activity Dates, allowing cost timing to reflect each
well’s place in the development plan.

Forecasts behave slightly differently. Decline start dates can be set to
use a Forecast Anchor instead of an explicit date. This anchor is then
linked to an Activity Date, which determines its start. 

## Defining Activity Dates at the Project Level

Activity Dates are defined at the project level and represent distinct
development milestones that costs or production are tied to. Default
Activity Dates such as *Planned Spud* and *On Production* are provided,
but they can be renamed or replaced unless already in use.

Activity Dates are configured through Tools \&gt; Global Project Data \&gt;
Activity Dates.

&gt; ⚠️ Important: Activity Dates cannot be deleted if they are referenced
&gt; in any well or lookup. This ensures consistency and prevents
&gt; accidental breakage of schedule logic.

This centralized configuration model allows teams to maintain a shared
definition of development phases while keeping timing logic aligned
across wells and lookups.

## Scheduling with Activity Dates through Lookups

Capital and operating cost lookups must define an anchor date for each
cost entry. Though not the only option, Activity Dates are the preferred
anchors, offering the most comprehensive scheduling functionality in Val
Nav. Costs are established relative to the selected anchor date.

The Cost Anchor Date can be set directly in the UI or in bulk using the
Capital and Operating Cost Deck spreadsheet import.

## Modeling with Wells & Groups

Well's can define their timing at the rescat level with Activity Dates
in the new Schedules data area, which allows scheduling through Common,
inheriting timing across multiple uncertainties (e.g., TP, TPP or P10,
P50, P90). When lookups are assigned to wells, they automatically
schedule based on the well’s Activity Dates.

To schedule forecasts based on Activity Dates, declines start dates must
be set to "Anchored" and a Forecast Anchor must be set to an Activity
Date. The Forecast Anchor is shared for all declines on a rescat. You
can also apply offsets to the activity date using the new Anchor Offset
input to stagger decline starts across products if needed for use cases
like modeling water breakthrough.

Anchored forecasts are now the default for newly created declines unless
the well is already set to manual, easing the configuration burden.

As always, Activity Dates and Forecast Anchors can be updated
efficiently using Val Nav’s bulk-editing tools: Data View, Spreadsheet
Import, Input Copier, and Data Manager. This allows you to reschedule
inventory for new development scenarios rapidly and reliably.

Lastly, consider the implications of anchored forecasts for producing
wells. Since the anchor is shared across all product and ratio declines,
they will shift together. When one product’s forecast is shifted, all
other forecasts dependent on the anchor will shift accordingly. Val Nav
automatically preserves each decline’s original parameters and Reserves
by walking the curve up or down as needed.

## Reconciliation & Schedules

Schedules are integrated into the reconciliation workflow to ensure
timing changes are clearly tracked and auditable.

### Option to Disconnect Lookups on Promotion

A project-level option allows users to realize lookup-driven values into
manual entries during promotion. This breaks the connection between the
well and both the lookup logic and Activity Dates for cost timing.

This is useful when promoting reserves that are under review and should
remain stable, even if the underlying development plan changes.

When disabled, the link to Activity Dates is preserved, allowing
schedule-driven costs to remain dynamic.

### The Schedule Step in Reconciliation

A dedicated Schedule step in reconciliation tracks:

- Changes to Activity Date definitions (e.g., new dates, renames)
- Updates to well-level Activity Date assignments

&gt; ⚠️ Note: This step does not reflect changes to lookup logic or cost
&gt; amounts. Those are managed in the Capital and Operating Cost steps.

This separation ensures that changes in when a cost or production event
occurs are managed independently from changes to what the value is,
providing clear accountability throughout development plan evolution.

Together, the Schedules feature and its reconciliation step offer robust
tools to model, manage, and track the timing of development across an
asset's lifecycle.

## Activity Dates and Pre-Existing Scheduling Functionality

Activity Dates represent Val Nav’s most comprehensive and flexible
approach to scheduling. While not yet at full feature parity with all
legacy scheduling tools, Activity Dates are intended to be the
foundation for future scheduling workflows.

### Timeline & Project Start

The Timeline tab is still driven by the Project Start date, which must
be set. If Activity Dates are in use, shifting the Project Start will
also shift Activity Dates accordingly, maintaining their relative
spacing and ensuring consistency across the development plan.

### Bulk Well Generator

The Bulk Well Generator automatically assigns Activity Dates to newly
generated wells if set on the seed well. Dates of a newly generated well
are determined relative from the rig-based start date determination and
the seed well's timing. If the Common Production Start option is used,
it sets the Activity Date used for the seed well’s Forecast Anchor.

### Adjust Dates

While the Adjust Dates tool includes an option to shift Activity Dates,
it is generally recommended to use more powerful tools like Data View
and Spreadsheet Import for managing Activity Date values. These options
offer greater flexibility, control, and bulk-editing capabilities.

### Schedules Entity

The lesser-used Schedules Entity is a container to group wells and
schedule them together alongside a stored constraint. Though it may
drive some confusion from their shared naming, it is not in direct
conflict with the Schedules data area.
