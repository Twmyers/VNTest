



# About Groups

Groups are a summation of production, forecasts, and capital costs for a
set of wells.

See [Create a Group or Rollup](../Create%20a%20Group%20or%20Rollup.md) and
[Modify a Group or Rollup](../Modify%20a%20Group%20or%20Rollup.md).

Groups are useful for evaluating commingled wells, injector/producer
pairs, units or shallow gas. When doing a pool material balance,
creating a group enables you to view the BHP and AOF tests for several
wells on one graph on Predictions \| P/Z.

A group becomes the main entity visible in the Entity Hierarchy. You can
expand the group to view the wells or other entities in the group. To
see groups, select the Wells and Groups,
or Groups view with the selector on the
main toolbar.

Production and forecast volumes associated with entities contained in a
group are not included in reserves for reconciliation purposes. Only the
group level production and forecast volumes are included.

See [Differences between Groups and Rollups](Differences%20between%20Groups%20and%20Rollups.md).

## Group Forecasts

When you create a group,
Value
Navigator creates a manual forecast (a summation of the child
forecasts). However, you can delete the manual forecast and best fit the
group as well. See
[Edit a Group Forecast](Edit%20a%20Group%20Forecast.md).

When you import new production, it is applied to the wells contained in
the group, not to the group itself. If you want the new production
included in the group, you must recalculate the group. See
[Recalculate a Group Forecast](Recalculate%20a%20Group%20Forecast.md).

## Group Economics

You can use groups to enter economic parameters for a set of wells as a
unit rather than entering economic parameters for individual
entities/wells and then aggregating those cases. When you create a group
from a selection of wells, the capital costs on the wells are summed at
the group level. However, no other economic parameters are included in
the group. You must build the economic case at the group level
(economics from the individual wells are not used at the group level).
Economics on individual wells are still visible and can be run or edited
at the well level.



If you want to see the total economic value of multiple wells, you do
not need to create a group or rollup. Instead, filter to the wells (if
necessary) and run economics at the folder level.
