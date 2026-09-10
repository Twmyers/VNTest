



# Create a Type Well

To create a type well

1.  In the Explorer, select the wells to use in the type well.
2.  Right-click, point to Create as, and
    select Type Well.
3.  In the *Create Type Well* dialog box, complete the following fields:



1.  | Field | Description |
    |----|----|
    | Name | Type well name |
    | Type Well Product | If the wells used to create the type well have oil and gas forecasts, but Gas is selected as the type well product, the oil forecasts are not used. The Auto setting determines the type well’s product automatically based on the production history of the wells being used. |
    | Start Date | The date to which the production history of all wells will be normalized. In PDP cases, the Start Date is equal to the [Project Options: Economics](../../Options/Project%20Options/Project%20Options%20Economics.md) by default. When a well is created from a Type Well in a non-PDP reserves category, the [Add or Adjust the Project Start Date](../../Entity%20Management/Schedules/Add%20or%20Adjust%20the%20Project%20Start%20Date.md) is set to the Type Well’s Start Date. |
    | Max shut-in months | If the number of months between a well’s last production date and the Current Month exceeds the number entered in max Shut In Months, the well is considered shut in. See [About Type Wells](About%20Type%20Wells.md) . |
    | Include non-producing months | If enabled, non-producing months are included in the Calendar Day Rate calculation. |
    | Calculation rate | **Calendar Day**: The average calendar day rate for each month. **Producing Day**: Ignores all non-producing hours on the child wells when generating volumes/rates on the type well.  |
    | Cut-off Point | See [About Type Wells](About%20Type%20Wells.md) |
    | Fixed Range | Specify a segment of the combined well history to use in the type well calculation. For example, you could choose to use only 2 years of data and also exclude the first month be entering **2** and **24** for the **Start** and **End** months, respectively |
    | Calculation Data | **History**: Only production history is used to create the type well. **History and Forecast**: History and forecast data are used to create the type well. |
    | [Plans](../../Entity%20Management/Plans/Plans.md) | Determines which plan to use in creating the type well forecast. |
    | Reserves Category | Only active if **History and Forecast** is selected in Calculation Data. Determines which reserves category to use in creating the type well forecast. |
    | Normalization Type | Select the field you want to use for normalization. |
    | Factor Type | Select Unfactored, Percentile (also specify a percentile value), P-Mean, or Custom Factors. |

2.  If you selected a **Factor Type** other than **Unfactored**, click
    **Advanced Options** and select the following options as required:
    | Option | Description |
    |----|----|
    | Method | Select **Aggregation** or **Selected Well**. This determines the type of statistical analysis performed to calculate weighting factors. |
    | Future drill count | Specify the number of wells that will be forecasted using the type well. Used to calculate weighting factors. |
    | High/Low EUR | Number of extrapolation points used to extend the trend line on the graph for high and low EUR. |
    | Distribution | Select **Smoothed** or **Actual** data. Determines how the trend line is calculated from source wells. |

3.  Click **OK**.



After creating the type well, you can edit the options above on the
**Type Well** tab by clicking **Options**.



Type Wells only consist of production history. To use the Type Well
history as the forecast for a new well, you must create a forecast for
the Type Well and then create the new well. See [Create a Well Using a Type Well](Use%20a%20Type%20Well%20to%20Create%20Other%20Wells/Create%20a%20Well%20Using%20a%20Type%20Well.md).

You can create copies of a type well and assign those copies different
factor types, such as P Mean, P10, or a custom factor percentage. See [Use a Type Well to Create Related Type Wells](Use%20a%20Type%20Well%20to%20Create%20Related%20Type%20Wells.md).
