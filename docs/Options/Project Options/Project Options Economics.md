

# Project Options: Economics

## Reference Date

Results are reported from this date. Remaining volumes, both actual and
forecasted, will include all values from the start of the month forward.
Discounted cash flows are calculated from this date.

## Economic Calculation Start Date

Economics are calculated from this date. In an unposted database, the
Economic Calculation Start Date and the Reference Date are the same by
default, but you can set the Economic Calculation Start Date before the
Reference Date (but you can’t set the Economic Calculation Start Date
later than the last posted date in a posted database).

## Last Year for Economic Monthly Output

Monthly economic values are stored in the database and displayed on
reports until the end of this year. After this year, annual values are
stored and displayed.

To store and display all annual values, set the last year for economic
monthly output to the year before the reference date.



Setting this year unnecessarily far in the future can drastically
increase your project size and slow economic calculations.



When a well terminates during a yearly forecast, the calendar day rate
is calculated from the partial year. The current year is not required to
be monthly.

## Maximum Life

Wells will not be forecast beyond this date, which is 60 years by
default. Value
Navigator can predict for a period of 200 years.

## Enable Abandonment Capital

If enabled in the Project Options, the Abandonment Capital textbox is
visible on **Economics \| General**.

## Enable Salvage Capital

If enabled in the Project Options, the Salvage Capital textbox is
visible on **Economics \| General**.

## Apply Variable Op Costs to Raw Gas Volumes

**Enabled**: When variable operating costs are entered for gas wells,
the Apply to Raw Gas checkbox on **Economics \| Prices & Costs \| Op
Costs/Other Revenue** is automatically selected.

**Disabled**: When variable operating costs are entered for gas wells,
the Apply to Raw Gas checkbox on **Economics \| Prices & Costs \| Op
Costs/Other Revenue** is not automatically selected.



Enabling or disabling this option after variable operating costs have
been added to gas wells does not alter the state of the **Apply to Raw
Gas** checkbox. It also does not alter any of the variable op cost
values.



## Report Negative product revenue as operating costs

Select this option to report negative product revenue.

## Discounting Settings

These are the discount rates displayed on economic reports. Any report
showing a single discount rate displays the rate entered in the middle
text box (discount rate 3). Discount Rates are calculated from the
Reference Date.

**Discount mid-month**: Always discount economic streams at mid-month.

**Discount mid-period**: Discount economic streams at mid-month until
the last period of monthly output and then switch to mid-year
discounting.

## Enable Economic Limit

If enabled, wells are terminated when economic results become negative.

If enabled in the Project Options, the Apply Economic Limit checkbox is
displayed on **Economics \| General** and enabled for all wells by
default. You can disable it for each well.

## Calculation Type

The selected calculation type is used to determine when the economic
limit is reached.

If Before Tax Cash Flow is selected, uneconomic development cases are
terminated and therefore do not appear in results. For entities with a
developed status (PDP, PD, PPDP, PPD, PPPDP, PPPD), abandonment capital
is not included in the BTCF calculation for economic limit. However for
undeveloped cases, abandonment costs are included in the economic limit
calculation. This enables PUD and PNP cases to correctly include
abandonment and salvage while maximizing DP cash flow cases.

## Discounting

The selected discounting rate is automatically used to determine the
economic limit when a new well is created.

## Allow Negative Wedge Results

If enabled, the wedge calculation result remains as is, even if it is
considered uneconomic. If you allow negative wedges, then TP is the
difference between the wedge and PDP even if it is uneconomic on a
cumulative cash flow basis.

If disabled, the wedge calculation is ignored if it is considered
uneconomic. The result is set to 0 and a report is not displayed. If
negative wedges are not allowed, the uneconomic wedge is removed and the
TP case falls back to PDP.

## Capital Actuals

**Run economics on forecast only**: Economics are run only on forecasted
capital costs.

**Run economics on blended costs**: Economics are run on forecasted and
actual capital costs (imported from
Execute
or another source). See [Run Economics on Blended Capital Costs](../../Execute%20Integration/Run%20Economics%20on%20Blended%20Capital%20Costs.md).

## 
