



# Understanding the Common Reserves Category

The Common reserves category provides you a single place to enter values
that you want to apply to all reserves categories or plans. In other
words, if an entity’s working interest is the same for all reserves
categories, you only need to enter it in Common—the value will
automatically be inherited by all other reserves categories or child
plans.

However, you can also override any reserves category or plan with a
value that is different from Common. So if you want all reserves
categories except one to use the same working interest, you can enter
the value in Common and override it in the one category. See
[Override Inherited Values](Override%20Inherited%20Values.md)

It isn't necessary to have the Common reserves category selected to edit
it. As long as the values you are entering are inherited directly from
Common, edits to them are also applied to Common, regardless of which
reserves category you are currently working in.

The default behaviour for the Common reserves category and the
relationship between it and the other categories is different in new
projects versus upgraded projects.

In new projects, all relevant tabs are linked to Common by default.

When you upgrade a
Value
Navigator project, all input values that can be linked to Common
are configured as overrides—they are not linked to Common.

To link the values to Common one tab at a time, see
[Reset Overridden Values](Reset%20Overridden%20Values.md).

To link the values on several tabs (or the entire project) at once, see
[Remove Inputs](../Plans/Remove%20Inputs.md).

## Input Values

Only the following tabs contain values that can be inherited from
Common:

| Tab | Subtabs |
| --- | --- |
| Economics | General |
| Interests &amp; Royalties |
| Prices &amp; Costs (and all subtabs) |
| Predictions | P/Z |
| Volumetrics |
| Data\|Plant |


## Data Inheritance

Data entered in Working-Common is inherited by other reserves categories
and plans through intervening plans and reserves categories, as
displayed in the grey message bar below.



![](../../Images/Understanding-the-Common-Reserves-Category-1.jpg)



In the example above, the current plan/reserves category (New Plan
2-PDP) inherits data from Working-Common.

If you override an intervening plan/reserves category (New Plan 1-PDP,
in the example below), the inheritance from Common is interrupted, and
data is inherited from the overridden plan/reserves category, as
displayed below.



![](../../Images/Understanding-the-Common-Reserves-Category-2.png)



If you override New Plan 2, it no longer inherits data from any other
plan/reserves category, as displayed below.



![](../../Images/Understanding-the-Common-Reserves-Category-3.png)



If you reset New Plan 2, it reverts to inheriting its data from the next
closest link in the inheritance chain.



![](../../Images/Understanding-the-Common-Reserves-Category-4.png)



If you reset New Plan 1, it reverts to inheriting data from
Working-Common, as does New Plan 2.



![](../../Images/Understanding-the-Common-Reserves-Category-5.png)



For more information about how inherited and overridden values are
displayed, see *Inherited and Overridden Values*, below.

For more information about overriding and resetting values, see
[Override Inherited Values](Override%20Inherited%20Values.md) and
[Reset Overridden Values](Reset%20Overridden%20Values.md).

Also see [Plans](../Plans/Plans.md).

## Inherited and Overridden Values

When you open a tab with values that can be inherited from Common, one
of three information bars is displayed on the tab, as described below.

## Values Inherited Directly from Common

The yellow information bar indicates that values on this tab are
inherited directly from Working-Common, as displayed in the breadcrumbs.



![](../../Images/Understanding-the-Common-Reserves-Category-6.jpg)



To override the values on this tab and enter values in Working-PDP,
click Override.

To edit the values in Working-Common, you can make your edits in the
current plan and reserves category (Working-PDP).

## Values Inherited Indirectly from Common or other Plans/Reserves Categories

The grey information bar indicates that values on this tab are inherited
indirectly from Working-Common (through Working-PDP and New Plan 1-PDP)
or that the values are inherited from another plan/reserves category, as
displayed in the breadcrumbs.



![](../../Images/Understanding-the-Common-Reserves-Category-7.png)



To override the values on this tab and enter values in New Plan 2-PDP,
click Override.

To edit the source of the values on this tab (Working-Common, in this
example), click Edit Source.

## Overridden Values

The green information bar indicates that values on this tab are not
inherited from any other plan or reserves category. The green
information bar is displayed when you are viewing Common or when you are
viewing any other tab that has overrides.



![](../../Images/Understanding-the-Common-Reserves-Category-8.jpg)



To remove the overrides (in any reserves category other than Common),
and enable a tab to inherit values from its source, click
Reset.
