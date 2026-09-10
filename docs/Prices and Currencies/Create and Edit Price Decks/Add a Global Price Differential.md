

# Add a Global Price Differential

By default, the Stream prices are linked to the Henry Hub or WTI prices.
Changing the Henry Hub or WTI price will cascade that change through all
of the prices linked to those stream prices, applying any differential
that has been entered on the individual stream price level. Grey
backgrounds on fields in a stream price indicate that the value is
entered manually and will not be affected by changing a higher-level
stream price. You can also change a stream price value by adding a new
differential, or typing over an existing differential.

Differentials on the Prices tab are
applied only to the current entity, but differentials you create in the
price deck are applied to all entities using the stream price to which
you applied the differential. Differentials you create in the price deck
are not displayed on the Prices tab--only
the result price is displayed.

To add a differential in the price deck, the stream price must be linked
to a parent price. If no parent price exists, you can change the price
by typing over the value in the Results column. If a differential
already exists, you can type over the values in the grid.

Differential inflation is applied (to differentials in the price deck
and prices on the Prices tab) according to the *Inflation of Price
Differentials* rate specified in the price deck under *Inflation*.
Removing the differential inflation value from the price deck removes
inflation for all differentials.

To add a price differential

1.  Open the Price Deck Editor from Tools
    \&gt; Global Project Data \&gt;
    Price Decks or by clicking
    Edit Price Decks on
    Economics \| Prices & Costs \|
    Prices.
2.  Select Stream Prices in the top left of the editor.
3.  Select the Stream price to which a differential is to be added.
4.  Click Add under
    Differentials at the bottom of the
    grid.
5.  Name the differential, select the differential type, and click
    OK to create a differential column in
    the prices grid.
6.  Enter the differential value in the new column and click
    Save and
    OK.
