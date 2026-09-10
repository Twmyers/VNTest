

# Currency Inheritance and Reporting Behavior

The currency assigned to entities and used in economic calculations
depends on the configuration of the project currency, the entity's
country, and the entity's currency.

By default, entities inherit the currency of their country, if one is
specified in the entity properties. You can override this inheritance by
changing the Entity Currency from Default
(*country currency*) to the currency you want the entity to use.
If a country is not specified for the entity, it inherits the Project
Currency, found in Project Options (US Dollars by default).
Value
Navigator has three countries and currencies by default (US,
Canada, and Euro), but you can create more.

When you run folder-level economics or when you run economics on a
selection of entities with different currencies,
Value
Navigator converts all currencies to the Project Currency.

 
