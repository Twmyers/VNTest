

# Configure Reserves Categories

As of Value
Navigator 2020, you can configure reserves categories , including
all the components, relationships, groups, and resource classes.
Value
Navigator supports complex models with contingent and prospective
resources, such as a full PRMS model or company-specific variants.
However it also enables you to simplify your reserves
categories: Planning groups who don’t split PDP and PUD wells, or
SEC-reporting clients who don’t need a P+PDP forecast, can remove any
unused categories.



By default,
Value
Navigator's usual reserves category functionality is used. Note
that PNP has been renamed PDNP.



The addition of custom reserves categories has resulted in changes to
the Reserves Category window in the bottom left of the interface. See [Use the Summary, Properties, and Inputs Windows](../Entity%20Management/View%20and%20Organize%20Entities/Use%20the%20Summary%20Properties%20and%20Inputs%20Windows.md).

## How do custom reserves categories work?

You can configure reserves categories with the Reserves Categories
dialog box. To customize your project's reserves categories you can add
your own categories, components, groups or resource classes or simply
select a template.



## Categories, Components, and Groups

In the Reserves Categories window you specify four tabs (if you're not
using templates, described below):

- **Reserves Categories**: The element of technical and economic
  modeling, which may map one-to-one to a component (e.g., PDP, PUD), or
  to a summation/total (e.g., TP = PDP + PDNP + PUD)
- **Components**: The fundamental increments of volume/value
- **Groups**: The groupings of reserves categories for capturing ranges
  of uncertainty (Proved, Probable, Proved + Probable, etc.) and for
  reporting
- **Resource Classes**: The highest division, to capture development
  maturity (e.g., Reserves, Contingent, Prospective), used exclusively
  for reporting purposes

## Reserves Categories Templates

Instead of configuring your own reserves categories, you can simply
apply one of the templates below:

- **Val Nav Classic**(default): Classic Val Nav reserves categories
  (note that PNP has been renamed PDNP)
- **Val Nav Classic + Simple Contingent**: Classic Val Nav categories
  plus one level for each of contingent and prospective resources (no
  contingent sub-classes)
- **Val Nav Classic + PRMS**: Extend classic Val Nav to a full PRMS
  model with contingent resource sub-classes
- **Simplified**: SEC-style: Simplified model without 1P/2P/3P
  equivalents of all wedges
- **Simplified + Contingent**: Extend the SEC-style model with one level
  each of contingent and prospective resources
- **Low-Best-High**: An alternative model with only low, best, and high
  cases, with no fallback or wedges
- **Blank**: All data removed for starting from scratch
- **GLJ**: For those clients with GLJ as their reserves evaluator, a
  system using the GLJ naming conventions (A, B1, B2, etc.)

To customize reserves categories

1.  Go to Tools \&gt;
    Global Project Data \&gt;
    Reserves Categories.
2.  If you simply want to use a template, click
    Apply Template. Select a template and
    click Yes to apply it. Go to step 4.
3.  Do one of the following: 
    | To | Do this |
    |----|----|
    | Add a reserves category | On the Categories tab, click Add. |
    | Add a component | On the Components tab, click Add. |
    | Add a group | On the Groups tab, click Add. |
    | Add a resource class | On the Resource Classes tab, click Add. |
4.  Edit the properties for each reserves category as needed. See the
    filed descriptions below.
5.  Click OK.

Below are descriptions of the properties on the Categories tab.

| Property | Use | How it is calculated |
|----|----|----|
| Name | Only in reports because they can get long. |   |
| Helps user figure out acronyms (e.g. PDP) | User input |   |
| Abbreviation | Used everywhere else | User input |
| Group | Grouping in reports and in the UI |   |
| Traditionally separates P1, P2, P3, P+P, P+P+P | User input |   |
| Components | Indicates which components are part of the reserves category | User input |
| Description | Gives Quorum or the user even more space to describe the reserves category, as the name has a 50-character limit | User input |
| Fit class | Determines which set of user options should be used for fitting a forecast in this category. Traditionally used to let ValNav create more conservative forecasts at 1P and more optimistic forecasts at 2P and 3P | User input |
| Has inputs | Whether the reserves category allows input. |   |
| Is generally synonymous with IsCalcTotal. | User input |   |
| Has Reserves Record | Whether the reserves category can be balanced and posted. | User input |
| Is Developed | Whether the reserves category is should behave like a developed project in the economic calculation (money has already been spent, so abandonment and salvage are guaranteed), or an undeveloped project (costs are not yet committed, and the entire project can be scrapped without penalty) | User input |
| Is Producing | Whether the reserves category behaves like historical actuals. (e.g. assume that the forecast must happen) |   |
| Rescats with this flag (and siblings in the same maturity) will be auto-fit during production import. | User input |   |

 
