



# Create a Common Termination Entity

To create a CTE

1.  Do one of the following:
    | If | Then |
    |----|----|
    | You have organized your entity hierarchy by Field (all wells and your cost entity are in the same folder), | In the entity explorer, right-click the folder level of the field you want to create as a CTE, point to **Create As** and select **Common Termination Entity**. |
    | You have filtered to your wells and cost entity, | Right-click the folder level of the field you want to create as a CTE, point to **Create As** and select **Common Termination Entity**. |
2.  In the Common Termination Entity dialog box, edit the **Entity
    Properties** and/or **Custom Fields**, if required.
3.  Select the following options for Child Results:
    | Option | Description |
| --- | --- |
| Honour economic limit on child entities | This option tends to maximize the value of a CTE. The child entity will terminate at the earlier of the calculated common termination date or its own economic limit. |
| Ignore economic limit on child entities | This option tends to maximize the volume produced by a CTE.The child entity will terminate at the calculated common termination date only. The child entity might be run beyond its economic limit, incurring costs out to the common termination date.Note: If you select this option and run economics on this well individually it will still run to the CTE’s termination date. To run the well to its own economic limit, select the option above before running economics for the entity. |
| Apply termination date to children | Enabled: The CTE date is applied to the child entities. Disabled: The CTE date is not applied to the child entities. For analysis purposes, disabling this setting makes it possible to determine what is causing the common economic limit to occur. : This setting should remain enabled unless you want to determine what is causing the economic limit to occur. |

4.  Select one of the following options for Negative Wedges:
    | Option | Description |
    |----|----|
    | Use project options | Use the setting in [Allow Negative Wedge Results](../../Options/Project%20Options/Project%20Options%20Economics.md#Allow). |
    | Allow | Always allow negative wedges in the calculation |
    | Do not allow | Never allow negative wedges in the calculation |

    

    The Negative Wedges option only applies to the CTE as a whole. Child
    calculations always allow negative wedges.

    
5.  Click **OK**.

## Reserves Plan Summary Window

The Reserves Plan Summary window displays reserves category information
for the CTE and child entities. Inputs on child entities are entered
independently of the CTE, and not saved on the CTE. Use the **Refresh
Summary Grid** button to load the entity input reserves categories.

- Inputs on child entities (![](../../Images/Create-a-Common-Termination-Entity-1.png)): Indicates reserves
  category inputs for child entities
- Economic results status (![](../../Images/Create-a-Common-Termination-Entity-2.png)): Indicates economic output
  for the CTE



The summary grid is blank by default. The current reserves category is
highlighted when you refresh the grid.
