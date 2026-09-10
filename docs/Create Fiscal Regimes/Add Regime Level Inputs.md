



# Add Regime-level Inputs

A regime-level input applies to all entities that use the regime.

This procedure is performed on the **Edit** tab in the **Fiscal Regimes
Editor**. To open the editor, click the **Tools** menu, point to
**Global Project Data** and select **Fiscal Regimes**.

To add a regime-level input

1.  Beneath the input list, click **Add** and select **Regime-level
    Input**.
2.  Type a name for the input and click **OK**.
3.  Complete the following fields:
    | Selection | Description |
| --- | --- |
| Input Style | Single value: Creates a field for one value.Â Recurring: Creates a date grid that repeats the entered value until a new value is entered. Non-recurring: Creates a date grid that does not repeat the entered value. |
| Data type | Select Number or Date. |
| Unit Type | Select the Unit Type. |
| Calc. unit | Select the Calculation unit. |
| Input unit | Select the Unit to use for the Input. |
| Result Stream | Optional. Determines the field in which the results are displayed on reports. |
| Report Factor | This field is only displayed if you specify a Result Stream. The Report factor is applied to the specified Result Stream. Select 1, Working Interest, or Working Interest/Net Revenue Income. |
| Custom Result | Specify the Create Custom Results Fields you want to hold the result data. This field can also be displayed on reports you create in the Report Designer. |
| Custom Factor | This field is only displayed if you specify a Custom Result. The Custom Factor applies to the specified Custom Result Field. Select 1, Working Interest, or Working Interest/Net Revenue Income. |
| Allocation | This field is only displayed when you specify a Custom Result or Result Stream. Allocation is available on Ring Fence regimes. A Result stream or Custom result at the ring fence level is allocated back to the entity level. It is meant as an approximation of the relative contribution of any one entity to the ring fence total. Select one of the following: Equal Values: The ring fence value is allocated back to child entities equally based on the number of entities. Proportional: The ring fence value is allocated back to child entities based on the relative value of a specified basis. See Basis, below. |
| Basis | This field is only displayed when Proportional is selected for Allocation. You can select a default allocation basis from the list or you can select one that you created (in the Allocation Basis folder). See Create an Allocation Basis |
| Values | Enter the input value(s). The values you enter are used for all entities using the regime. |

4.  Click **OK** or go to the next step, [Create a Calculated Variable](Add%20Variables%20to%20a%20Fiscal%20Regime/Create%20a%20Calculated%20Variable.md) or [Create a Trigger Variable](Add%20Variables%20to%20a%20Fiscal%20Regime/Create%20a%20Trigger%20Variable.md).
