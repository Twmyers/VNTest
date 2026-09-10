



# Recalculate a Group Forecast

By default, the forecast on a group is a summation of the child wells
forecasts.

You can recalculate the group forecast if you have:

- Deleted it to do a best fit on the group, but want to return the
  manual summation forecast
- Edited the forecasts of child wells and want to incorporate these
  changes into the group forecast
- Updated production on the child wells
- Added or deleted wells from the group

To recalculate a group forecast

1.  Do one of the following:
    | To | Do this |
    |----|----|
    | Recalculate one group, | On **Predictions \| Declines**, click ![](../../../Images/Recalculate-a-Group-Forecast-1.jpg) and click **Recalculate**. |
    | Recalculate more than one group, | Select the groups you want to recalculate (or filter to them). From the **Entity** menu, select **Recalculate Groups**. |
2.  Select the following options from the **Recalculate Group** dialog
    box, as required:
    | Option | Description |
    |----|----|
    | Recalculate production history | Updates the production history, but does not move the group forecast. |
    | Recalculate forecast | Recalculates the group forecast (summation of child wells). If there is a decline, it is deleted unless *Skip groups with declines* is selected. |
    | Skip groups with declines | Use this option to prevent Value Navigator from replacing a best fit decline with a manual (summation) forecast. |
    | Recalculate volumetrics recoverable | Recalculates volumetrics recoverable. |
    | Recalculate P/Z recoverable | Recalculates P/Z recoverable. |
    | Recalculate Depths | Recalculates depths |
    | Recalculate Capital | Recalculates capital |
    | Recalculate child groups | If the group contains groups (child groups) they are only updated if this option is selected. |
    | Current reserves category | Applies the selected options to the current reserves category. |
    | All reserves categories with forecasts | Applies the selected options to all reserves categories with a forecast. |

    

    When a group has child groups, if some of these child groups have
    declines at the child group level (instead of a summation forecast),
    it is possible to sum these child group declines by selecting **Skip
    groups with declines**. This allows you to keep any child group
    declines intact.

    
3.  Click **OK**.
