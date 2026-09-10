

# Create a Calculated Variable

A calculated variable is the result of a static calculation that you
create in the Formula Editor. A calculated variable can use entity-level
and regime-level inputs. Calculated variables can be used in trigger
variables.

This procedure is performed on the **Edit** tab in the **Fiscal Regimes
Editor**. To open the editor, click the **Tools** menu, point to
**Global Project Data** and select **Fiscal Regimes**.

To create a calculated variable

1.  Beneath the input list, click **Add** and select **Calculated
    Variable**.
2.  Type a name for the variable and click **OK**.
3.  Complete the following fields:
    | Selection | Description |
| --- | --- |
| Input Style | Series or single value |
| Data type | Data type |
| Unit Type | Unit Type |
| Calc. unit | Calculation unit |
| Result Stream | Optional. Determines the field in which the results are displayed on reports. |
| Report Factor | This field is only displayed if you specify a Result Stream. The Report factor is applied to the specified Result Stream. Select 1, Working Interest, or Working Interest/Net Revenue Income. |
| Custom Result | Optional. Specify the Create Custom Results Fields you want to hold the result data. This field can also be displayed on reports you create in the Report Designer. |
| Custom Factor | This field is only displayed if you specify a Custom Result. The Custom Factor applies to the specified Custom Result Field. Select 1, Working Interest, or Working Interest/Net Revenue Income. |
| Allocation | This field is only displayed when Proportional is selected for Allocation. Allocation is available on Ring Fence regimes. A Result stream or Custom result at the ring fence level is allocated back to the entity level. It is meant as an approximation of the relative contribution of any one entity to the ring fence total. Select one of the following: Equal Values: The ring fence value is allocated back to child entities equally based on the number of entities. Proportional: The ring fence value is allocated back to child entities based on the relative value of a specified basis. See Basis, below. |
| Basis | This field is only displayed when Proportional Allocation is selected. You can select a default allocation basis from the list or you can select one that you created (in the Allocation Basis folder). See Create an Allocation Basis . |
| Category | Optional. The variable is only applied in this production category. |
| Subcategory | Optional. The variable is only applied in this production subcategory. |

4.  Click ![](../../Images/Create-a-Calculated-Variable-1.png) next to the **Formula** field to create the
    formula for the variable. See
    [Create Formulas for Regime Variables](../Create%20Formulas%20for%20Regime%20Variables.md).
5.  In the **Formula Editor**, create the formula by moving formula
    elements to the formula window.
6.  Click **OK**.
