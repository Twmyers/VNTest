

# The Use of 1+WOR in Value Navigator

Value
Navigator is unique among its peers in the way it combines Arps
decline equations for oil, 1+WOR, and Oil + Water to forecasts wells
with bottom water or waterflood. The purpose of this topic is to
describe the interactions and how they may be used to obtain an enduring
forecast.

## Forecasting Oil Using 1+WOR

In Value
Navigator, we choose to plot log(1+WOR) versus cumulative oil
production. If we expect the relationship to be a straight line, then
the equations take the form of an Arps exponential shown below with
1+WOR replacing rate and cumulative oil production replacing time. The
area under the curve is the cumulative oil plus water forecast. Thus,
the cumulative form of the Arps equation may be used to calculate a
fully integrated value for the cumulative oil plus water production.

1+WOR=((oil+water))⁄oil \| oil=((oil+water))⁄((1+WOR) )

(1+WOR)=(1+WOR)\_i exp(d_i cum oil) \| (oil cut)=(oil cut)\_i exp(-d_i
cum oil)

In the equations, it may be seen that 1+WOR is equal to the inverse of
oil cut. When plotting oil cut versus cumulative oil production, the
equations are identical except that the slope (d_i) has the opposite
sign and the oil cut intercept is the inverse of the 1+WOR intercept. We
choose 1+WOR over oil cut so that the oil and 1+WOR declines are
opposing, making it easier to separate the data.

If the 1+WOR relationship is exponential and the fluid (oil + water)
rate is constant, the oil decline will be harmonic. If the 1+WOR
relationship is harmonic with constant fluid rate, the oil decline will
be exponential. The fitting algorithms will allow any Arps equation for
log(1+WOR) versus cumulative production subject to constraints placed in
the user fit options. There are standard graphs available to view oil
cut instead of 1+WOR.



The dialog box for 1+WOR is shown on the left. The terms Q_i and Q_f
refer to the initial and final values for 1+WOR. Q_f is truly a final
value in the sense that the well forecast will stop when the final value
is reached.

The decline factors are the initial and final slope. In nominal terms,
the formula is shown below.

d_i=(-ln\[(1+WOR)\_2⁄(1+WOR)\_1 \])/((〖cum oil〗\_2-〖cum oil〗\_1 ) )

If the user setting for decline is specified as secant or tangent and
the equation is not exponential, then refer to
[Effective and Nominal Rates](Effective%20and%20Nominal%20Rates.md) help for the
appropriate conversion formulae.

The value shown for Max is the constant fluid rate that will be used in
conjunction with the 1+WOR decline to calculate the oil production rate
at any time. With a best fit, the constant fluid rate is calculated
iteratively to match the average of the most current three oil
production rates. If one of these three oil rates is an outlier compared
to the rest, it will be excluded from the average. Data with an oil cut
greater than 90% are excluded when calculating the best fit for 1+WOR.

If additional segments are required to obtain the correct forecast,
click the Add Forecast button. The additional segment will be linked by
rate, but one or more of the parameters will need to be altered to
identify when the additional segment is to commence. Parameters in the
additional segment will need to be modified for the desired results.

On the detailed oil card shown above, the volume of oil is shown for
each segment and the estimated ultimate recovery (EUR) is shown. This
value is for the segment and includes historical production from prior
years. If there is an overlap between the end of history and the start
of forecast, the program will choose the value identified in the project
options (general).

|  |  |  |
|----|----|----|
|  |  |  |

If a 1+WOR does not exist, it may be added by clicking the 1+WOR button
on the product card. This will open a 1+WOR card with a pre-set constant
1+WOR equal to the most current six-month average. A second click to Add
Decline will create an assisted forecast constrained to the user fit
setting options that have been set.

The other alternative is to simply alt-click on the graph close to the
1+WOR data. A best fit will be calculated using the fit options, but
this time the best fit will cover the date range (or equivalent
cumulative production range) from the click position to the most current
date. Because of the user intervention in selecting the date, the fit is
improved.



Often the fluid rate is not constant. In this case, the constant liquid
rate from the 1+WOR detail card (Max) may be replaced with an O+W (fluid
rate) forecast that may be added using either of the procedures that
were used for 1+WOR. From the following chart pair, it may be seen how
the O+W forecast alters and again improves the quality of the oil fit.



The O+W forecast that was automatically generated has a decline that is
a little too shallow. From visual inspection a steeper decline is fit by
drawing the decline (right click on the chart). This offers a slightly
improved oil forecast in terms of aligning with the historical data and
there are no more changes that can or should be made based on the use of
the 1+WOR curve.

The forecast is a technical one that will stop when 1+WOR reaches 250,
but it does not reach that value. Without an oil decline there is no
technical termination point, so the well continues to produce to the
year 2078 which is the [maximum
life](../../Options/Project%20Options/Project%20Options%20Economics.md#Maximum_Life_)
set in the project options. If a technical limit is desired, then one
would visit the data tab to discover the value for 1+WOR that
corresponds to the oil technical termination rate. An oil termination
rate of 2 would occur when the 1+WOR reaches 26.5.

## Forecasting Oil Using the Oil Decline

If there is no need to model the cost of water disposal and a water
forecast is not required for other purposes (i.e. material balance),
then we need only forecast the oil production. In this example there are
two, possibly three, forecasts that reasonable fit the data. These could
be reported as different reserve categories as shown in the graph, but
there is also the possibility of integrating these forecasts with 1+WOR
to refine the estimates.



## Integrating the Oil and 1+WOR Declines

If we have an oil decline and a 1+WOR decline (with or without O+W),
there are two ways to calculate oil production.
Value
Navigator calculates the oil rate using both methods and retains
the lowest rate of the two. If production bottleneck is the reservoir,
then the lowest oil rate will be calculated from the oil decline. If the
production bottleneck is upstream (limited pump capacity, choke size or
pipeline capacity), then the oil rate will be calculated from the 1+WOR
decline.

Sometimes it is known that there is no bottleneck, and it is simply
desired to use the 1+WOR to forecast water production with no
integration. This is accomplished by deleting the constant fluid rate on
the 1+WOR detail card or in bulk in the declines tab of the entity view.
This will set Max to zero, and it will be ignored in the calculation
algorithm, forcing oil to be calculated from the oil decline. Water is
then calculated using the following formula.

water=oil \[(1+WOR)-1\]



In the above chart, we see the integrated forecasts with some bizarre
behavior at long time, so let’s deal with the bizarre behavior first.
The oil decline is set to terminate at 10 bbl/d, and it does but the
well does not terminate production at this point because the forecast is
able to continue using 1+WOR. The software needs to integrate the
termination, choosing to stop production at the first terminal point
(oil decline or 1+WOR decline) or have the user explicitly identify
which decline takes precedence relative to terminating all forecasts for
the well. For the moment, the solution is to set a proper termination
rate for oil, and if the 1+WOR runs longer then force its termination
with an appropriate final rate. The chart with the corrected termination
point is shown.



The following example is taken from a different well. In early time the
oil forecast is harmonic with a constant fluid production rate. These
are two indicators that the forecast is derived from the 1+WOR decline.
This would also be a signal to shoot a fluid level on the well to
determine whether the well is pumped off, and if not examine the
economic value of installing a larger pump. At the end of 2027, the
decline switches back to exponential and the fluid rate begins to
decline. The well is now producing all that the reservoir can deliver
and the oil rate is calculated using the oil decline.



## Miscellaneous

The [hot key
function](../../Customize%20the%20User%20Interface/Keyboard%20Shortcuts.md)
in Value
Navigator is very effective in fine tuning the decline
parameters. The magnitude of the shift with each press of the arrow key
depends on the magnitude of the parameter. Often the decline factor for
ratios like 1+WOR become very small, making the shift increments too
large. This may be corrected by adjusting the display unit. For ratios
that are plotted against cumulative production, set the slope (decline
factor) to %/unit of cum oil on the graph. If the graph has units of
mbbl, then the slope units would be %/mbbl.

If there is an O+W forecast and no 1+WOR forecast, then the O+W curve
will be used to calculate water production as O+W – oil, or oil
production as O+W – water.
