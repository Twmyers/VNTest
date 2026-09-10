



# Best Fit or Refit Wells

When you best fit or refit a well,
Value
Navigator determines how much history to use in calculating the
decline. To best fit or refit a well from a point in history or from a
selection of history, see
[Best Fit or Refit a Decline from a Point](Best%20Fit%20or%20Refit%20a%20Decline%20from%20a%20Point.md) or [Best Fit or Refit a Decline from a Selection](Best%20Fit%20or%20Refit%20a%20Decline%20from%20a%20Selection.md).

When you best fit a well,
Value
Navigator determines whether the decline should be hyperbolic,
harmonic or exponential. When you refit a well,
Value
Navigator maintains the well‚Äôs current decline type.

To best fit or refit all the wells in your project, select the highest
level folder in the Entity Explorer and follow the procedure below. If
you only want to best fit some wells, select the wells individually or
select the folder level that contains them or filter to them first.



Declines are created in reserves categories in accordance with the
decline parameters specified for each category in your [User Options: Product Specific](../../Options/User%20Options/User%20Options%20Product%20Specific.md). For example,
selecting All Developed Producing in the Best Fit Options (below) will
only create a decline in those reserves categories if you have entered
decline parameters for them in the User Options. You can access the User
Options by clicking the button in the bottom left corner of the Best
Fit/Refit dialog box or by selecting **Options** from the **Tools**
menu.



To best fit or refit wells

1.  In the entity explorer, select the entity or the folder level that
    contains the wells you want to best fit or refit.
2.  Do one of the following:
    1.  On the **Predictions** menu, click **Best Fit or Refit**
    2.  Click ![](../../Images/Best-Fit-or-Refit-Wells-1.jpg)¬†on **Predictions \| Declines** and click
        **Best Fit** or **Refit**
3.  In the **Best Fit/Refit** dialog box, select the appropriate
    options, below.
    | Option | Description |
| --- | --- |
| Date Range for Fitting |
| All Data | Value Navigator automatically determines how much production history is needed to calculate a decline for each well. |
| Recent | Value Navigator only goes back the entered number of months in production history and calculates a decline using that history. |
| Start of current fit to end of history | The fit is based on data from the beginning of the current fit to the end of production history. |
| Fit decline trends within the date range | When selected, Value Navigator looks for individual trends within the specified range. Trends are prioritized based on how recent they are and how much data they conform to. |
| Exponent Options |
| Find the best exponent based on user options | The exponent is determined using your User Options: Product Specific. |
| Keep the current exponent type | Maintains the well‚Äôs current exponent type. |
| Keep the current exponent value | Maintains the well‚Äôs current exponent value. |
| Fit using the exponent value of | Assigns the exponent the specified value. |
| Fit Options |
| Create or replace only the specified products | Only wells with the products selected under Products to Fit will have a best fit decline added. Wells with decline: Decline is replaced. Wells without decline: Decline is created. |
| Only fit the specified products if decline exists | Only wells with a decline and the products selected under Products to Fit will have a best fit decline added. Wells with decline: Decline is replaced. Wells without decline: No change. |
| Fit specified products; remove unchecked products | All selected wells are affected. Wells with the products selected under Products to Fit: Wells with decline: Decline is replaced. Wells without decline: Decline is created. Wells with the products not selected under Products to Fit will have their declines removed. |
| Special Fitting Methods* |
| Use special fitting when N &gt; | Special fitting is used when N is greater than the specified value. |
| Methods to use | Power Law q = qi¬ exp (-d‚àû t-di¬ tn), where di= d1‚ÅÑn |
| Stretched q = qi exp[-(t‚ÅÑt)n ] = qi¬ exp(-di¬ tn), where di=d1‚ÅÑn |
| Duong q = q_1 tD+ q‚àû |
| *Note on Special Fitting Methods If Value Navigator cannot find a fit for the method you selected, it falls back to other fit methods as described below: Duong and Stretched fall back to Arps Power Law Loss Ration falls back to Stretched then to Arps |
| Set d-infinity | Use this option to specify the d infinity term that is used in the Power Law Loss Ratio fitting instead of allowing Value Navigator to automatically calculate it when determining the fit. You can set this term for oil and gas separately. The default values are specified in User Options &gt; Fit Settings &gt; Product Specific &gt; Minimum nominal Df (Proved). The unit (Nominal/Eff.Sec./Eff.Tan.) is specified in User Options &gt; General &gt; Decline display settings. |
| Daily Data | ¬ |
| Fit daily data instead of monthly, when present | Fits daily data instead of monthly, when present |
| Fit Target |
| Name | Name for the forecast in the Decline Workspace. |
| Current reserves category | Creates the decline in the currently selected reserves category. |
| All Developed Producing | Creates the decline in PDP, P+PDP, and P+P+PDP. |
| Create in Decline Workspace | Selecting this option creates a decline in the Decline Workspace, in the fit class specified below. Assign each Best Fit a name so you can compare them in the Decline Workspace. See Create Multiple Forecasts on Predictions \| Workspace |

4.  Confirm the **Entity Count** to ensure you are best fitting or
    refitting the correct number of entities.
5.  Click **OK**.
