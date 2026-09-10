

# Specify a Change Record Sequence

The change record sequence is used to define the following:

- The order of the automated reconciliation calculation. Each
  calculation is net of the preceding step in the sequence.
- The order in which the results are reported on the Waterfall chart on
  Review \| Waterfall.
- The change record categories used for each change type. You do this by
  mapping data areas to change record categories (see the example,
  below).

The default change record sequence is determined by the project country
(in Project Options). You can simply use the default sequence or change
it to meet your specific reporting requirements. You can also set
sequences for different jurisdictions.

In the Change Record Sequence dialog box, you must map data areas to a
Change Record Category or leave them unmapped (Improved Recovery, for
example) in which case ARR will only assign that Change Record Category
via a Change Reason.

## Example

In the example below, the sequence is built using the default
Value
Navigator Change Record Categories and Summary Types.

You can create more Summary Types or Change Record Categories. See [Create or Edit Change Record Categories or Summary Types](../Review%20Change%20Records%20Overview/Create%20or%20Edit%20Change%20Record%20Categories%20or%20Summary%20Types.md).

Under Technical Revisions, changes to Declines, Plant Gas Properties or
a change in shared calculations will result in Change Records with a
Change Record Category of Technical Revision because all three input
areas are mapped to that category.

The Change Record Category Extensions and Improved Recovery is not
mapped to any inputs. This means that you should only expect change
records with a Change Record Category of Improved Recovery to be created
through a Change Reason of the same type, or by manually using the
Balance function. It also means all Extensions and Improved Recovery
records will be first in the sequence for charting/reporting.



## Input Areas Descriptions

See descriptions of the input areas below.

- **Reference date**: Applies the reference date of the evaluation. This
  will normally also change the discount date, thus changing BTCF NPV
  numbers.
- **Prices**: Applies both entity-level price data (price set, parent
  stream prices, differentials, and price overrides), as well as any
  changes to the price deck.
- **Operating costs**: Applies any modifications to operating cost
  definitions and any entity op costs.
- **Capital costs**: Applies any modifications to capital cost
  definitions and any entity cap costs.
- **General Economics**: Applies general economic data (COO/COS,
  abandonment, etc.). Excludes manual termination dates in the current
  period. Includes certain project options also. Cam to provide complete
  list.
- **Interests**: Applies any interest changes not captured in Ownership
  Increase or Ownership Decrease (e.g., sliding scales, tract/pooling
  factors, reversions, etc).
- **Ownership increase**: Applies new interests where a current-period
  start date is set, or where WI or NRI inputs increase versus prior
  period. Recommend to capture as acquisition.
- **Ownership decrease**: Applies interests where a current-period end
  date is set, or where WI or NRI inputs decrease versus prior period.
  Recommend to capture as disposition.
- **Manual termination**: Applies manual termination date changes where
  the new value is within the evaluation period (between posted date and
  reference date). Recommend to capture as disposition.
- **Regimes/royalties**: Applies any modified fiscal regime or Canadian
  royalty inputs. Also applies any relevant global project data (regime
  models, meter stations, facilities, custom result fields, etc).
- **Production**: Applies any new production history to the case (may
  not have an impact depending on the history/forecast overlap project
  option). Best captured as production variance.
- **Declines**: Applies any changes to the declines/wellhead data. Also
  applies new product and ratio definitions).
- **Plant gas properties**: Applies any to the plant gas properties
  (master gas analysis, gas losses, liquids extractions). Also applies
  new sour gas extraction limits from project options.
- **Shared calculation membership**: Applies the addition/removal of any
  wells to/from a shared calculation (CTE or ring fence).

To specify a Change Record Sequence

1.  Go to **Tools** \&gt; **Global Project Data** \&gt; **Change Record
    Categories**.
2.  Click **Change Record Sequence**.
3.  Select the appropriate Jurisdiction.
4.  Do one of the following:
    | To | Do this |
    |----|----|
    | To reorder the summary types, | Place your mouse over the section and drag it to a new location. |
    | To add a data area, | Click Add Area. |
    | To delete a data area, | Click the X next to the area. |
    | To change the change record category mapped to a data area, | Select a different change record category from the list. |
    | Specify that a Change Reason be used for a summary type instead of mapping to entity inputs, | Click Unmapped next to the Summary Type. |



1.  Click **OK**.
