

# Add Filters to Custom Table Reports

Adding filters to custom table reports limits the amount of data
presented in reports. By default, two filters are applied to all
reports: Scenario Group is null and Scenario is null. These filters
prevent scenario data from being reported on, if any scenarios exist in
the project. In most cases, you should also add filters to limit the
reserves categories and reserves statuses being reported.



You can override the scenario and entity filters when running a custom
report on the Reports tab.



The following procedure explains how to add a filter that will limit
data to the PDP reserves category.

To add a filter to a report

1.  In the Report Editor, drag **Res. Cat.** from the Fields and
    Formulas window and drop it in the Filters window.
2.  In the Filter Properties dialog box, select is equal to from the
    Show rows where the value list.
3.  From the Fixed Value list, select **Proved Developed Producing**.
4.  Select the following options, if required:
    | Option | Description |
    |----|----|
    | Show this filter in the list of filters | When you run the report, the filter is displayed in the Filters and Parameters window where you can manipulate its parameters. |
    | Show a list of value for this filter | A list of available values for the filter type is displayed in the Filters and Parameters window (if the previous option is selected). |
    | Allow “Show All” in list | The Show All option appears in the filter list in the Filters and Parameters window. Selecting Show All from the filter list turns the filter off and displays all results. |
5.  Click **OK**.



Only reserves categories that have had economics run appear in the
window.
