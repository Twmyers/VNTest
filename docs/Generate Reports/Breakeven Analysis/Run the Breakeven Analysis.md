



# Run the Break-even Analysis

To run the break-even analysis

1.  From the **Tools** menu, select **Break-even Analysis**.
2.  In the Break-even Analysis Options dialog box, select the following
    options:
    | Option | Description |
    |----|----|
    | Plan | Select a Plan. |
    | Reserves category | Select a reserves category and discount rate to use in the analysis. |
    | Discount rate | Discount rates in the list are specified in [Project Options: Economics](../../Options/Project%20Options/Project%20Options%20Economics.md). |
    | Inflation rate | This option inflates prices, using the input flat rate, for the break-even analysis only. |
    | Calculate on | This determines which NPV results columns are displayed in the results grid. The analysis generates results for before tax and after tax NPVs and then calculates a before tax and after tax break-even price. Both after tax and before tax are recorded for every iteration. This option only determines which NPV to try to get to 0. When running both results, first the before tax iterations are run all the way to the break-even factor. Then the after tax calculation will use the existing iterations to make a better initial guessing in calculating its results. |
    | Vary | Choose to vary oil prices, gas prices, or both. If both prices are varied, the calculation determines the break-even price for the primary product. **Oil prices**: Includes oil and liquids (excluding C2) par and reference prices **Gas prices**: Includes gas par and reference prices. C2 is varied with gas since C2 pricing is based on gas prices. **All prices**: Vary all prices above plus sulphur. |
    | Primary product | This determines which product price is highlighted in the results grid. |
    | Honour economic limit | When the limit checkbox is selected, the economic limit on an entity is honoured and the NPV’ at prices below break-even are zero. The graph display shows results trending to zero. When the limit checkbox is not selected, NPVs are allowed to run negative and the graph displays points on either side of zero. The solution displayed in this case is the break-even point for the technical forecast limit rather than the economic limit, and is likely to be higher. |
    | Benchmark | Select whether to standardize results to a benchmark price. When this option is selected, and a benchmark is specified, all results are referenced in this price. This enables you to compare results on entities that use different prices and entity level offsets. Running a break-even analysis at a folder level requires you to select a benchmark. To select a benchmark price, select the option then click **Set**. Select your benchmark price from the dialog box. |
    | Additional price points | Choose whether to include additional points on the results display. You can enter specific prices to display in the grid, calculate additional points around the break-even price, or both. Adding points gives you more information about price sensitivity. To add absolute price points, click ![](../../Images/Run-the-Breakeven-Analysis-1.jpg). |
3.  Click **OK**.

## Results

**Break-even Tab**Results are displayed on this tab for single
calculations. Entity results are displayed here, such as wells, groups,
and common termination entities. Folder level results are also displayed
on this tab.

**Comparison Tab**Results for all entities in the current selection are
displayed on this tab. This may be a folder, rollup, common termination
entity, type well, or bulk well schedule. Groups are not included as
child entities in a group and have no economic value of their own.

Selecting a point on **Comparison** graphs highlights the entity in the
hierarchy that corresponds to that selection.

## Reports

Clicking **Show Report** at the top left of the screen launches a Print
Preview window that displays results for the current tab in report form.
Graphs and grid displays are included in the report. Columns displayed
in the report grids depend on options selections.

See [Break-even Analysis Behaviour](Breakeven%20Analysis%20Behaviour.md) for more details
regarding: 

- Prices
- Single entity calculations
- Folder calculations
- Common Termination Entities (and children of CTEs)
