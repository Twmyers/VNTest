

# Project Options: General

## Company Name

This is the name that appears in reports and as the highest level folder
in the Entity Hierarchy.

## System Scenario Name

The default scenario name is \.

## Default Scenario

Select either \ (Project) or Reserves (jurisdiction).

## Project Currency

The project currency is used for:

- Entities you have not assigned a currency (in the entity properties)
- Reports on project-level or folder-level economics or on a selection
  of entities with different currencies

The currency assigned to entities and used in economic calculations
depends on the configuration of the project currency, the entity's
country, and the entity's currency.

By default, entities inherit the currency of their country, if one is
specified in the entity properties. You can override this inheritance by
changing the Entity Currency from Default
(*country currency*) to a different currency. If you don't
specify a country, the entity inherits the project currency.



See Also

- [Add a Country](../../Countries%20and%20Currencies/Add%20a%20Country.md#aanchor17)
- [Add a Currency](../../Countries%20and%20Currencies/Add%20a%20Currency.md#aanchor13)
- [Set the Country Currency](../../Countries%20and%20Currencies/Set%20the%20Country%20Currency.md#aanchor20)
- [Set the Entity Currency](../../Countries%20and%20Currencies/Set%20the%20Entity%20Currency.md#aanchor14)
- [Set the Project Currency](../../Countries%20and%20Currencies/Set%20the%20Project%20Currency.md#aanchor12)



## Project Label

This is an alias name for a project. After you re-start the project, the
name you enter will appear on the menu bar, before the path of the
project.

## BOE Ratio

This is the default ratio that will be used to convert gas to the
equivalent barrels of oil.

## CO2 Threshold

CO2 is left in the gas stream if the percentage is less than the CO2
Threshold. See [Default Process Loss with CO2 and
H2S](../../Forecasting/Enter%20and%20Edit%20Plan%20Data/Inlet%20Outlet%20Sales%20and%20Total%20Loss%20Calculations.md).

## CO2 Allowable

CO2 is removed from the gas stream if it exceeds the CO2 Allowable. See
[Default Process Loss with CO2 and
H2S](../../Forecasting/Enter%20and%20Edit%20Plan%20Data/Inlet%20Outlet%20Sales%20and%20Total%20Loss%20Calculations.md).

## Last Year for Technical Monthly Output

Monthly technical values are stored in the database and displayed on
reports until the end of this year. After this year, annual values are
stored and displayed.

To store and display all annual values, set the **Last year for
technical monthly output** to the year before the reference date as well
as the **Maximum technical life (Dec 31)**.



Setting this year unnecessarily far in the future can drastically
increase your project size and slow economic calculations.



When a well terminates during a yearly forecast, the calendar day rate
is calculated from the partial year. The current year is not required to
be monthly.

## Use Overlapping Production History instead of the Forecast

This option determines which production rates to use when generating
forecast volumes. If you import production data, but don’t set the
forecast start date to the end of production, there is an overlap of
history and forecast data. If you enable this option, the production
history volumes are used in calculations instead of the forecast
volumes.

## Default Country

The country selected here affects the display of fields such as country,
state, and province. In projects with United States set as the default
country, for example, State will appear as a column header instead of
Province.

The default country is automatically used when creating new wells. This
country is also automatically selected in the Countries dialog (Tools \&gt;
Set up \&gt; Countries).

## Default State/Province

The selected default state/province is automatically used when a new
well is created.

## Default Forecast Mode

You can configure whether the default forecast mode is Total or
Incremental. See [Create an Incremental Forecast](../../Forecasting/Create%20and%20Edit%20Declines/Create%20an%20Incremental%20Forecast.md).

## Default Surface Loss

This is the default surface loss percentage applied to all new wells
added to the current project (shown on **Predictions \| Declines**).
