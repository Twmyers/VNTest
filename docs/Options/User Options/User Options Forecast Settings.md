



# User Options: Forecast Settings



## Max Shut-in Months

If the number of months between the last production date and the Current
Month exceeds the number entered in max Shut In Months, the wells are
considered shut in. Shut-in wells are not auto-forecasted on import and
do not receive an economic case when economics are run. By Default,
shut-in wells do not receive data copied to them from the Economic Input
Copier.



This setting is also used when performing a best fit.



## Generate Forecast from Last Production Month

If this option is enabled, all wells in the project are forecasted from
their last month of production. If this option is disabled, all wells
are forecasted from the Current Month. If a well’s last month of
production is prior to the project’s current month, but within the
maximum shut-in months, there will be a gap between the last month of
production and the start of the forecast.

This setting affects how the current month is set. See
[Set the Current Month](../../Create%20Projects/Set%20the%20Current%20Month.md).

Enabling this option is recommended when a project contains U.S. wells,
where there is a large difference between each well’s last month of
production.



This setting is also used when performing a best fit.



## Backfit

- **Only show the backfit on graphs when there is no auto fit source**:
  If enabled, the backfit is not displayed on wells that have an auto
  fit source. On wells with manual declines, the backfit will be
  displayed.

## Date Range for Fitting

These options control how
Value
Navigator auto-forecasts wells.

- **All data**:
  Value
  Navigator automatically determines how much production history
  is needed to calculate a decline for each well.
- **Recent**:
  Value
  Navigator only goes back the entered number of months from the
  [Set the Current Month](../../Create%20Projects/Set%20the%20Current%20Month.md) and calculates a decline
  using that history.
- **Start of current fit to end of history**: The fit is based on data
  from the beginning of the current fit to the end of production
  history.
- **Fit decline trends within the date range**: When selected,
  Value
  Navigator looks for individual trends within the specified
  range. Trends are prioritized based on how recent they are and how
  much data they conform to.

## Inclining or Shallow Decline Transition (Oil, Gas, Condensate)

These options limit the length of inclining or very shallow forecasts.
Inclining forecasts and shallow forecasts (defined by the value entered
in **Minimum Decline**) are limited to the number of months entered in
**Incline period duration** and **Flat period duration**. After the
duration, a new exponential decline segment is started at the rate
entered in Default nominal slope. See
[User Options: Product Specific](User%20Options%20Product%20Specific.md).

## Daily Data



- **Allow fitting from daily data**: Enable or disable fitting for daily
  data
- **Use daily data until**: Sets the transition point at which monthly
  data is used in fitting instead of daily data.

For the rest of the options, see the *Inclining or Shallow Decline
Transition* section, above.

## Product Specific



Value
Navigator calculates an exponential, harmonic, and hyperbolic
decline for oil, 1+WOR (inverse of oil cut), condensate, and gas. It
then determines the average on-time, the maximum producing rates, and
estimates the reserves associated with each of the possible decline
types. A best fit is then produced.

Exponential, Hyperbolic, or Harmonic declines can be enabled or disabled
with the check boxes. Enabling these decline types under PDP (Proved
Developed Producing) or PPDP (Proved + Probable Developed Producing)
generates a decline in those reserve categories.



Declines are not calculated if the Exponential, Hyperbolic, and Harmonic
boxes are all deselected.



The **Min**. and **Max**. Exponents specify the Ni range allowable for
the hyperbolic decline. Specifying a maximum Ni of less than 1.0
prevents harmonic declines (Ni=1).

The Default parameters are used when inclining or shallow decline best
fit slopes are created.

The **Use exponential transition** setting controls when hyperbolic or
harmonic declines transition to an exponential decline.
