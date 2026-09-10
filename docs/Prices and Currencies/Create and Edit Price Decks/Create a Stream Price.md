



# Create a Stream Price

Stream Prices are used by
Value
Navigator to calculate the sales price for each product. You can
use stream prices from evaluator’s price decks, or create your own
custom stream prices. The Sample price deck included with
Value
Navigator includes benchmark stream prices that you can use as a
basis for creating your own stream prices. Stream prices can be grouped
into Price Sets and applied to an entity or a set of entities. See
[Create a Price Set](Create%20a%20Price%20Set.md) Stream prices use sparse data entry; you need only enter
your price one time, and
Value
Navigator will continue to use that price until another is
entered.

When a custom stream price is created in a particular price deck, it
will have value only when that price deck is selected.

By default, the Stream prices are linked to the Henry Hub or WTI prices.
Changing the Henry Hub or WTI price will cascade that change through all
of the prices linked to those stream prices, applying any differential
that has been entered on the individual stream price level. Grey
backgrounds on fields in a stream price indicate that the value is
entered manually and will not be affected by changing a higher-level
stream price. You can also change a stream price value by adding a new
differential, or typing over an existing differential.

To create a stream price

1.  In the Tools menu, select **Global
    Project Data** \&gt; **Price Decks**.
2.  In the Price Deck Editor, click **Stream Prices** (on the left).
3.  In the editor window, select the folder level where you want the new
    stream price.
4.  Under the Stream Prices window, click **Add**.
5.  Enter a name and click **OK**.
6.  To the right of the Stream Prices window, specify the Country,
    Province/State, (these fields are already selected if you chose the
    appropriate folder level) Product, and Currency.
7.  Do one of the following:
    | Options | Go to |
    |----|----|
    | Use a base price as a starting point, and adjust it with differentials. | Step **8**. |
    | Enter prices in the date array, starting at the Reference Date. | Step **14**. |
8.  Under **Parent Price**, click **Set** and select a price.
    

    If the Stream Price Currency does not match the Parent Price
    currency, an exchange column is automatically inserted between the
    Parent and Result price and the exchange rate is applied.

    
9.  Under **Differentials**, click **Add**.
10. Enter a name and **Description**.
11. Select a **Differential Type** and click **OK**.
12. Enter the differential value in the new column between the
    **Parent** price and the **Result** price.
13. **Optional**: To add a price escalation, complete the steps below.
    See [Escalate Prices](../../Entering%20Economics/Enter%20Prices%20and%20Costs/Escalate%20Prices.md) for more information.
    1.  In the **Escalation %** row in the header area of the **Result**
        column, enter an **Escalation %**.
    2.  In the **Result** column, enter a new price in the year the
        escalation begins.
14. The cell is displayed with a grey background to indicate a manual
    price override. The **Escalation %** is applied to the override and
    begins one year after the override.
15. Click **Save**.
