



# Enter a Payout Reversion or Incentive Balance and Effective Date

You can enter a payout reversion value or incentive balance and specify
the date at which it is effective on **Economics \| Interests &
Royalties.** See
[Enter Reversions](Enter%20Reversions.md) **or**
[Select Incentives](Select%20Incentives.md)

## Effective Date and the Economic Calculation Start Date

You can set the Effective Date to be on or after the Economic
Calculation Start Date specified in Project Options. An Effective Date
prior to the Calculation Start Date will be ignored and the Calculation
Start Date will be used in calculations.

The Effective Date you enter for a payout reversion or incentive is
affected by the Economic Calculation Start Date in the following ways:

- If you move the Economic Calculation Start Date to be later than the
  Effective Date of any entities, you should adjust the Effective Dates
  and associated values or balances to be equal to or later than the
  Economic Calculation Start Date. Otherwise, the Effective Date will be
  ignored, and balances will be decremented as of the Economic
  Calculation Start Date.
- If you return the Economic Calculation Start Date back to a point on
  or before the Effective Date, the balance is decremented from the
  Effective Date again.
- Balances are not automatically adjusted when you move the Economic
  Calculation Start Date. If balances are removed or adjusted, they
  cannot be restored.

## Payout Reversion and Incentive Behaviour

If you enter an Effective Date for a payout reversion or an incentive:

Payout reversions are only calculated using the Reversion Value you
enter. All prior capital entered on the case is ignored. If the
Effective Date is not entered, capital entered on the case will be
included. Incentives are assumed to be in place in all calculation steps
prior to the Effective Date. The balance entered on the case is
decremented from that date. The incentive is not capped at a maximum
value.

## Reporting on Effective Dates and Balances

Use the **Calc. Date Adjustment Report** to identify entities affected
by a change to the Economic Calculation Start Date.

Use the **Remaining Balance—Incentives and Remaining
Balance—Reversions** reports to display remaining balances as of the
Reference Date.
