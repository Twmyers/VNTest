



# Enter Abandonment and Salvage Costs

Abandonment and Salvage amounts can be entered in two places:
**Economics \| General** and **Economics \| Prices & Costs \| Capital
Costs**.

## Abandonment and Salvage in Economics \| General

Abandonment and salvage amounts entered under **Abandonment and
Salvage** on **Economics \| General** are inflated from the **Economic
Calculation Start Date** according to the rate entered for **Capital
Cost Inflation**. See [Edit Inflation](../../Prices%20and%20Currencies/Create%20and%20Edit%20Price%20Decks/Edit%20Inflation.md).

The full abandonment and salvage amounts are incurred, regardless of the
**Chance of Success**. However, if the COS is less than 100%, the
failure portion is incurred immediately while the remaining amount is
incurred after the well becomes uneconomic. If you enter a delay
(months) the amounts are incurred that number of months after the well
becomes uneconomic.



When entering abandonment or salvage costs on a well with no forecast,
you must enter the costs as an override in any reserves category other
than Common. When abandonment and salvage are entered in Common on a
well with no forecast, the costs are not calculated and do not appear in
reports.



To enter an abandonment or salvage amount on Economics \| General

1.  Go to **Economics \| General**.
2.  Under **Delayed Abandonment** or **Delayed Salvage**, enter the
    amount in the **Cost** field.
3.  If you are delaying the costs, enter the delay in months (full
    months only) in the **Delay** textbox.

## Abandonment and Salvage Amounts in Economics \| Prices & Costs \| Capital Costs

Abandonment and salvage amounts entered on the **Capital Costs** tab are
inflated from the date they are entered according to the rate entered
for **Capital Cost Inflation** (unless **Prevent Inflation** is selected
on the **Capital Costs** tab). See **Adjust Inflation**.

If a Chance of Success is entered on **Economics \| General** and
abandonment or salvage is entered as a failure cost, the failure portion
is only incurred on the date that it is entered. For success costs, only
the success portion of the cost is incurred on the date it is entered.



When entering abandonment or salvage costs on shut –in wells, you must
enter the costs as an override in any reserves category other than
Common. When abandonment and salvage are entered in Common on a well
with no forecast, the costs are not calculated and do not appear in
reports.



See
[Enter Capital Costs](Enter%20Capital%20Costs.md)
