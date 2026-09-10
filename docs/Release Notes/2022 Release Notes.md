

# 2022 Release Notes

## New Features

### Oil Cut Forecasting

Forecasting production for waterfloods or conventional reservoirs with
drive mechanisms like bottomwater drive, edgewater drive, or combination
drives can be complex. Value Navigator is unique among its peers in the
way it integrates oil, total fluid, and now, oil cut forecasts for these
reservoirs where production can be characterized by changing fluid
composition. Building on existing 1 + WOR forecasting functionality, its
reciprocal, oil cut, can now be forecasted with Arps parameters to
define fluid composition relative to cumulative oil production. Oil cut
offers a more intuitive fluid composition forecasting experience since
it follows the same visual queue as normal Arps declines including a
decline to the cumulative total on the X-axis on rate/cum graphs.

Base uses include pairing with an oil forecast to define the water
production or with a max fluid rate to define the oil forecast. However,
Val Nav enables you to go a few steps further. An oil + water forecast
decline can also be generated to act as a variable maximum liquid rate,
thus effectively modeling fluid handling constraints, while still
honoring the supplied oil cut curve. Finally, all three curves can be
supplied. By taking the lowest oil rate defined by either the oil curve
or oil cut decline, Val Nav has the intelligence to determine whether
the production bottleneck is reservoir capacity or an upstream limit
like limited pump or pipeline capacity or choked back production.



## Polygonal Map Selection

You now have more fidelity when selecting wells from the map with a new
polygon selection mode. When enabled, a simple click-and-hold with the
mouse enables you to draw lines while the "B" key creates a break in the
line to draw a new polygon side. When finished, releasing the mouse sets
the polygon and selects the wells inside.



## Enhancements

- Extended the Spreadsheet Import tool to import against Vendor IDs so
  that supplementary information from any data source can easily be
  appended with a simple import.
- Extended database connection functionality to utilize the
  SQL-recommended driver that supports TLS 1.1+.
- Extended product ratios auto-forecasting algorithm to Oil Cut. This
  adds yet another level of sophistication and efficiency to
  conventional reservoir and waterflood-based forecasting. These fits
  can be triggered in all the same ways as other products and ratios: \*
  Alongside regular product fits via the fitting dialog (Predictions \&gt;
  Best Fit and Predictions \&gt; Refit) \* Via graph interactions
  (alt-click, ctrl-click, etc., or via right-clicking) \* On import of
  production data Fit options are available in the user options (Tools
  \&gt; Options \&gt; User Options).
- Extended allowable characters to support recommended naming in Azure
  SQL database deployments. Extended password limits to match the max
  allowable password length in the current database type.
- Extended database connection functionality to Azure SQL databases
  configured with integrated Active Directory.
- Broadened Val Nav workflow-oriented approaches to forecasting. Ratio
  constants can now be updated in bulk. Previously tied to production
  imports, these ratio updates can now be triggered by the user with a
  new Predictions dialog to rapidly update secondary product forecast
  projections with ease.

## Bug Fixes

- Fixed an issue where long price deck names would not display correctly
  in Scenarios configuration dialog.
- Fixed an issue where floating point precision could cause a recently
  balance entity to remain very slightly unbalanced.
- Fixed an issue where imported Jurisdictions could create change
  records.
- Fixed an issue where imports of old User Options file could cause an
  error.
- Fixed an issue where imported Jurisdictions could remove the opening
  balance, posted date, and change records.
- Fixed an issue where map coloring would not render the first time the
  map was configured.
- Fixed an issue where certain Vendor IDs were incorrectly parsed when
  attempting to match to data sources.
- Fixed an issue where Condensate daily data was not properly aggregated
  when a Group was calculated.
- Fixed an issue with improper units displaying in the type well
  normalization field.
