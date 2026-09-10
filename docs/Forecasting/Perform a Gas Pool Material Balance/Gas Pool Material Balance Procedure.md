



# Gas Pool Material Balance Procedure

## Create a group of the wells to include in the analysis

When doing a pool material balance, enables you to view the BHP and AOF
tests for several wells on one graph on **Predictions \| P/Z**.

## Deselect wells that don’t belong to the pool

Looking at pressures on the Pressure vs. Time graph is a quick way to
find wells that don’t belong to a pool. Identify wells with an initial
pressure that is too high compared to the pool at the time of the
pressure test.

On the **P/Z** and **Pressure** graphs, each pressure test is labelled
with a letter that corresponds to a well in the Rollup. The first
production month for each well is also indicated at the bottom of the
**Pressure vs. Time** graph with a tick mark and a letter.

Wells are listed with their corresponding letters on **Predictions
\|P/Z\| Well Information**. The **Well Information** tab also lists each
well’s pool and first production month.

You can deselect entities on the **Well Information** tab by removing
the checkmark in the **Use** column or you can .

## Deselect unwanted gas analyses and recalculate the Master Gas Analysis

All available gas analyses for the group are averaged to produce a
Master Gas Analysis. Gas analyses appear in **Predictions \| Gas
Analysis**.

To deselect a gas analysis, remove the checkmark in the Use column of
Predictions \| Gas Analysis. When gas analyses are modified on the
Predictions \| Gas Analysis tab, the Master Gas Analysis is
automatically recalculated. However, when viewing gas analyses for a
group that has been modified, the Master Gas Analysis is not
automatically recalculated. When a Master Gas Analysis needs to be
recalculated, it is displayed with a grey background. To recalculate the
Master Gas Analysis, click Recalculate Master Gas Analysis on
Predictions \| Gas Analysis.

Each component for a gas analysis can be sorted for easy detection of
anomalous values. To sort the component columns, click in the white area
above each column header. Depending on whether you sort the column
ascending or descending, anomalous values will go to the top or bottom
of the column.

Also see [Add a Gas Analysis](../Enter%20and%20Edit%20Plan%20Data/Add%20a%20Gas%20Analysis.md).

## Enter the Corrected Pool Datum and Recovery Factor (or Abandonment Pressure)

The Corrected Pool Datum and Recovery Factor are entered on
**Predictions \| P/Z \| P/Z Information**. The Pool Datum, if available,
can be found in **Predictions \|P/Z\| Well Information**.

If a new abandonment pressure is entered, the recovery factor is
automatically recalculated. When a recovery factor is entered, the
abandonment pressure is automatically recalculated.

## Deselect unwanted BHP tests

BHP Tests, when available, are in **Predictions \|P/Z\| BHP Tests**. To
find wells with insufficient shut in times, click in the white area
above the **Shut In Time** column header. Depending on whether you sort
the column ascending or descending, times will be listed from longest to
shortest or shortest to longest.

BHP Tests can be deselected individually or in bulk from either the
**BHP Test** tab, or from either graph on the **P/Z** tab.

To deselect individual BHP Tests from the **BHP** tab, in the **Use**
column, deselect the test’s checkbox.

To bulk deselect BHP Tests from the BHP tab

1.  Left-click the first well and hold the mouse button.
2.  Drag the mouse over the wells you want to deselect to highlight
    them.
3.  Right-click inside the highlighted area and click **Deselect** from
    the menu.

To deselect individual BHP Tests from the P/Z graphs:
Double-click the test
(![](../../Images/Gas-Pool-Material-Balance-Procedure-1.png)). The red
square becomes
![](../../Images/Gas-Pool-Material-Balance-Procedure-2.jpg). Clicking
![](../../Images/Gas-Pool-Material-Balance-Procedure-2.jpg) reselects the
BHP Test. 

To bulk deselect BHP Tests from the P/Z graphs

1.  Right-click on the graph.
2.  Point to **Select Points** and click **Deselect Below Line**.\
    The mouse cursor changes to a pen.
3.  Hold the left mouse button and draw a continuous line above all the
    tests you wish to deselect and release the mouse button. All points
    below the line are deselected.

## Explanation of BHP Test Data

- **Cum to Date** is calculated from the cumulative gas production at
  the test date.
- **Z factor** is calculated with information from the master gas
  analysis and the **P/Z Information** tab. When calculating Z factor,
  Value
  Navigator needs to calculate the pressure for the test. The
  pressure is calculated using a pressure that depends on which Pressure
  Source is selected.
  | Pressure Source       | Value used as “pressure” in calculations |
  |-----------------------|------------------------------------------|
  | Extrap Pressure Datum | Extrap Datum Pressure                    |
  | Extrap Pressure Mpp   | Extrap MPP Pressure                      |
  | Pressure Datum        | Well Datum Pressure                      |
  | Pressure Mpp          | MPP Pressure                             |
  | Run Depth Pressure    | Run Depth Pres                           |
  | Otherwise             | 0                                        |

If **Corrected pool datum** is set,
Value
Navigator uses it to correct the pressure before proceeding with
the calculation.

Other variables used when calculating the Z factor:

- Kelly Bushing
- Pool Datum Correction
- Formation Temperature
- Current Depth, Reference Depth
- Gas Gradient, Run Depth Gradient, Gas Column Correction

## Edit the declines of the child wells

If you intend to use the manual forecast of a group, the declines of
each well should be validated. See [Edit a Group Forecast](../../Entity%20Management/Groups%20and%20Rollups/About%20Groups/Edit%20a%20Group%20Forecast.md).

Clear the manual decline and [generate a group forecast](../../Entity%20Management/Groups%20and%20Rollups/About%20Groups/Batch%20Recalculate%20Group%20Forecasts.md).

When you create a Group,
Value
Navigator automatically creates a manual forecast (a summation of
the child wells’ forecasts). If you want a forecast based on the
combined history of the child wells, you can best fit the Group.

To delete a forecast

1.  In the **Reserve Category** window, click **Remove All Data**
    (![](../../Images/Gas-Pool-Material-Balance-Procedure-3.jpg)).

To best fit a Group

1.  Delete the manual forecast by clicking **Remove All Data**
    (![](../../Images/Gas-Pool-Material-Balance-Procedure-3.jpg)) in the **Reserve Category** window.
2.  On the **Predictions** menu, point to **Best Fit**. See [Best Fit or Refit Wells](../Create%20and%20Edit%20Declines/Best%20Fit%20or%20Refit%20Wells.md).

To return to the manual forecast, on **Predictions \| Declines**, click
**Recalculate**.

## Adjust the group final rate

When a group is best fit,
Value
Navigator uses the minimum rate (Qf) found in . Validate the
minimum rate on the group forecast as this Qf may not be appropriate for
the group.

## Link the decline to the P/Z analysis

See [Link a Decline to a P/Z or Volumetric Analysis](../Create%20and%20Edit%20Declines/Link%20a%20Decline%20to%20a%20PZ%20or%20Volumetric%20Analysis.md).
