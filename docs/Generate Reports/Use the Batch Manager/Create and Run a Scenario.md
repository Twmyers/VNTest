



# Create and Run a Scenario

Scenarios can be run on entities or folders to compare the results when
variables are altered. For example, the Economics Summary report could
be run on a potential acquisition using three different price decks to
see how the rate of return is affected by the different prices.

The following variables can be adjusted when running scenarios:

- Abandonment Capital
- Economic Limit
- Use escalating price
- Saskatchewan Capital Surcharge
- Price Deck
- Capital costs
- Operating costs
- Price Template
- Chance of Success
- Chance of Occurrence
- Price Factor
- Operating Cost Factor
- Capital Cost Factor
- Production Factor
- Companies

To create a scenario

1.  Do one of the following:
    1.  In the **Tools** menu, point to **Global Project Data**, and
        click **Scenarios**.
    2.  On the **Scenarios** tab of the **Batch Manager**, click
        **Edit** **Scenarios**.
    3.  Click **Scenarios** on the **Reports** tab.



2.  In the **Scenarios** dialog box, click **Add**.
3.  Enter a name and click **OK**.
4.  Under Scenario visibility, select one of the following options:
    | Option | Description |
    |----|----|
    | Project scenario | The scenario is part of the project and is available to all users.   |
    | User Scenario | The scenario is only available to the user who created it, in the current project. |
5.  Under **Scenario parameters**, select one of the following options:
    | Option | Description |
    |----|----|
    | Shared | The scenario is applied to all plans. |
    | Per plan | The scenario is only applied to the specified reserves plan or plan. |
6.  If you selected **Per Plan**, select the reserves plan or plan you
    want to apply the scenario to. If you selected **Shared**, go to
    step 7.
7.  Modify the Calculation Options, Calculation Dates, Risk, and
    Sensitivity.
    | Option | Description |
    |----|----|
    | InflationOverride | The value you enter overrides all inflation values (general, operating cost, capital cost, price deck inflation, etc.). |
    | Selected Companies | Companies that are disabled in the **Companies** dialog box in **Global Project Data** are also disabled in the **Scenarios** dialog box. For Jurisdiction scenarios, only companies selected in the Jurisdiction’s Selected Companies are used. You cannot change a Jurisdictions Selected Companies in the Scenarios dialog box. To change a Jurisdiction’s Selected Companies, see [Create Jurisdictions](../../Reserves%20Management/Jurisdictions/Create%20Jurisdictions.md). |
    | Cost, Price, and Production Factors | The value you are entering is a percentage. To increase a value by 20%, enter *120*; to decrease a value by 20%, enter *80*. |



9.  Click **OK**.

To run a scenario

1.  Do one of the following:
    1.  On the **Tools** menu, click **Batch Manager**.
    2.  On the toolbar, click the **Batch Manager** icon
![](../../Images/Create-and-Run-a-Scenario-1.png).



2.  In the **Batch Manager**, click the **Entities** tab.
3.  Under Entity Selection Mode, click Quick Selection.
4.  Under **Entities to report**, select the entities and/or folders you
    want to report on.
5.  Under **Reserves categories**, select the reserves categories you
    want to report on.
6.  On the **Report Options** tab, select the currency you want to use
    for the batch.
7.  Do one of the following:
    | To                            | Do this       |
    |-------------------------------|---------------|
    | Save the batch for future use | Go to step 8. |
    | Run the batch                 | Go to step 9. |
8.  Click **Save as Batch**, enter a name, and click **Save**.\
    The created batch is selected in the batches list.
9.  On the Scenarios tab, under Scenario Selection Mode, select
    Calculate selected scenarios.
10. Under **Scenarios**, select the scenarios you want to run.
11. For **Recalculation** mode, select one of the following options:
    1.  Calculate if necessary
    2.  Do not calculate
    3.  Force recalculation



12. For **After calculation**, select one of the following options:
    | Option | Description |
    |----|----|
    | Do not show reports | The Print Preview is not displayed after the scenario is calculated. |
    | Show print preview | The Print Preview is displayed after the scenario is calculated. |
    | Print selected reports | If you have already created a report list, the reports you selected are automatically printed after the scenario is calculated. See [Create a Report List](Create%20a%20Report%20List.md). |
13. Click **Run**.
14. In the **Print Preview**, click a report to view or click
    **Select/Manage Reports** to create a report list.
