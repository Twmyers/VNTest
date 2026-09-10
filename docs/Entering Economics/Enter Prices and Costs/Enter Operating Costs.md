



# Enter Operating Costs

Enter capital costs on individual wells on **Economics \| Prices & Costs
\| Capital Costs** or in bulk using the Data View grids or a spreadsheet
import. Security permissions are required to use some of the bulk
editing tools. Contact your administrator for access.

## Interests

When you enter capital costs, enter the gross amount. The working
interest or facility interest share is calculated according to the
percentage entered for **Operating Cost Interest** or
Facility Interest on **Economics \|
Interests & Royalties**. See [Enter a Working Interest](../Set%20Up%20Interests%20and%20Royalties/Enter%20a%20Working%20Interest.md).

- **Working Interest costs**: costs that a company has an interest in.
- **Facility Interest costs**: costs for a facility that a company has
  an interest in.

## Inflation

Inflation is applied to each cost according to the operating cost
inflation rate entered in the Price Deck Editor. The default operating
cost inflation rate is zero. See [Edit Inflation](../../Prices%20and%20Currencies/Create%20and%20Edit%20Price%20Decks/Edit%20Inflation.md).

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



## GCA (Gas Cost Allowance) Costs

If a cost category name is appended by (GCA) it is used to calculate GCA
allowance.

## Costs on Shut-in Wells

When entering operating costs on shut-in wells, you must enter the costs
as an override in any reserves category other than Common and change the
**Cost Type** to **Cost/Time**. When operating costs are entered in
Common or inherited from Common on shut-in wells, the costs are not
calculated and do not appear in reports.

## Entering Operating Costs

To enter operating costs

1.  Go to **Economics \| Prices & Costs \| Operating Costs** and click
    **Add Costs**.
2.  Move the costs you want to add from the **Available Costs** window
    to the **Selected Costs** window by double-clicking them.
3.  Click **OK**.
4.  Enable Show cost details at the
    bottom of the costs grid.
5.  Select or enter the following information at the top of the cost
    column:
    | Option | Description |
| --- | --- |
| Name | You can rename the cost, but the new name only applies to the cost on the current entity. However, you can also create custom costs. See Create Custom Capital or Operating Costs. |
| Prevent Inflation | Prevents inflation. |
| GOR Deductible | Applies the cost to any GORR entered on Economics \| Interests &amp; Royalties. |
| Escalation % (annual) | Escalates the cost by the percentage you enter (in addition to the operating cost inflation rate in the price deck). |
| Apply to Raw Gas | (Variable costs only). Applies cost to raw gas. |
| Cost Type | Cost/Well/Time: (fixed op costs only) For each well in the well count, the cost value is applied per time period (per day, month, or year). Cost/Time: (fixed op costs only) Regardless of the number of wells, applies the cost value per time period. Cost/Volume: (variable op costs only) Cost is applied per volume of associated product. |
| Unit | Select a daily, monthly or annual unit. |

6.  In each cost column, enter the gross amount of each cost next to the
    appropriate date.

## Tips

- You can change the date display under Display Mode, in the bottom
  right corner of the screen.
- You can copy costs to other wells using the [Copy an Entity](../../Entity%20Management/Create%20and%20Edit%20Wells/Copy%20an%20Entity.md).
