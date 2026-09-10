



# Enter Capital Costs

Enter capital costs on individual wells on **Economics \| Prices & Costs
\| Capital Costs** or in bulk using the Data View grids or a spreadsheet
import. Security permissions are required to use some of the bulk
editing tools. Contact your administrator for access.

## Categories

You can enter capital costs in three categories: Common, Success and
Failure.

- **Common costs**: incurred regardless of success or failure.
- **Success costs**: incurred only if the project is successful.
- **Failure costs**: incurred only if the project fails.

## Interests

When you enter capital costs, enter the gross amount. The working
interest or facility interest share is calculated according to the
percentage entered for **Capital Cost Interest** or
Facility Interest on **Economics \|
Interests & Royalties**. See [Enter a Working Interest](../Set%20Up%20Interests%20and%20Royalties/Enter%20a%20Working%20Interest.md).

- **Working Interest costs**: costs that a company has an interest in.
- **Facility Interest costs**: costs for a facility that a company has
  an interest in.

## Inflation

Inflation is applied to each cost according to the capital cost
inflation rate entered in price deck. The default capital cost inflation
rate is zero. See [Edit Inflation](../../Prices%20and%20Currencies/Create%20and%20Edit%20Price%20Decks/Edit%20Inflation.md).

You can prevent inflation on individual costs by selecting
Prevent Inflation at the top of each cost
column. To see the Prevent Inflation check box, you must select
Show cost details at the top of the costs
window.

## Salvage and Abandonment

To enter delayed abandonment or salvage, go to
Economics \| General. See [Enter Abandonment and Salvage Delay](../Enter%20General%20Economic%20Data/Enter%20Abandonment%20and%20Salvage%20Delay.md).

When entering abandonment or salvage costs on a well with no forecast,
you must enter the costs as an override in any reserves category other
than Common. When abandonment and salvage are entered in Common on a
well with no forecast, the costs are not calculated and do not appear in
reports.

## Incremental Costs

When you use the incremental forecasting mode (see [Create an Incremental Forecast](../../Forecasting/Create%20and%20Edit%20Declines/Create%20an%20Incremental%20Forecast.md)), you only need
to add the incremental portion of your cost. However, you must create
the incremental cost by clicking Override
in the Information bar at the top of the costs grid. See
[Enter Incremental Costs](Enter%20Incremental%20Costs.md).

If you are using incremental forecast mode on the well, the Base cost
(from the PDP reserves category) is displayed with a light blue bar
below the cost name. The new incremental cost is displayed with a dark
blue bar.



Incremental costs and forecasts are not used in the PDP reserves
category.



## Costs on Shut-in Wells

When entering capital costs on shut-in wells, you must enter the costs
as an override in any reserves category other than Common. When
operating costs are entered in Common or inherited from Common on
shut-in wells, the costs are not calculated and do not appear in
reports.

## GCA (Gas Cost Allowance) Costs

If a cost category name is appended by (GCA) it is used to calculate GCA
allowance.

## Entering Capital Costs

To enter capital costs

1.  Go to **Economics \| Prices & Costs \| Capital Costs** and do one of
    the following: 
    | To | Do this |
    |----|----|
    | Add a regular capital cost, | Click Add Cost. |
    | Add an incremental capital cost, | Click Override in the information bar and then click Add Cost. |
2.  Select a Cost stream. You can also
    change the cost stream later by selecting it at the top of the cost
    column.
3.  Move costs from the **Available Costs** window to the **Selected
    Costs** window by double-clicking them.
4.  Click **OK**.
5.  At the top of the grid, enable Show cost
    details and complete the following options as required: 
    | Option | Description |
    |----|----|
    | Name | You can rename the cost, but the new name only applies to the cost on the current entity. However, you can also create custom costs. See [Create Custom Capital or Operating Costs](Create%20Custom%20Capital%20or%20Operating%20Costs.md). |
    | Cost Stream | Select Common, Success, or Failure. |
    | Prevent Inflation | Enable this option to prevent inflation for the current cost. |
    | Reversion Factor | Control how much of the cost is included in a payout reversion calculation. If you want to exclude the cost from the payout reversion calculation, set the **Reversion Factor** to **0**. |
    | Unit | Select a unit. |
6.  In each cost column, enter the gross amount for regular capital
    costs or the incremental amount for incremental costs next to the
    date on which it is incurred.

## Tips

- You can change the date display under **Display Mode**, in the bottom
  right of the screen.
- You can copy costs to other wells using [Copy Input to other Entities](../../Entity%20Management/Create%20and%20Edit%20Wells/Copy%20Entity%20Data.md)
- You can rename costs by typing in the **Name** field at the top of the
  column. However, this does not rename this cost for the entire
  project.

For the GCA classes associated with each capital cost, see
[Capital Cost Allowance (CCA) Classes](Capital%20Cost%20Allowance%20CCA%20Classes.md).
