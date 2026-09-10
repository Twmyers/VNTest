

# Batch Manager Overview

You can create report batches that consist of wells, folders, plans and
reserves categories. This enables you to generate entity-level and
folder-level reports at the same time, in several reserves categories
and plans. If you run several batches simultaneously and select
Consolidate Results, the batch results are added together. Batch Manager
can also be used to create scenarios that allow the application of
factors to the existing entity properties.

Entities and folders can be selected in the Batch Manager independently
of entities or folders selected in the Entity Explorer. If you apply a
filter to the project, the filter also applies to the entities visible
in the Batch Manager.

Reports in Batch Manager are produced only for entities/folders that
have been selected with a check mark. Selecting an entity will produce a
report for that entity. Selecting a folder will produce a report for the
folder level. The folder level report will run the economics on all
wells in the folder that are visible in the Entities to report list in
Batch Manager, but will display only a summary report at the selected
folder level. To exclude wells from a folder level report in Batch
Manager, apply a filter to the project before opening Batch Manager.



Once you have run a batch, you can select reports or create customized
report lists and use them with your batches. Use caution when using
Batch Manager - output tables can fill up quickly!

## Reserves Categories in Batch Manager

In addition to the nine categories for which production forecast and
economic parameters can be entered, the economic value of other reserves
categories can be determined.

- Wedge results for PNP, PUD, P+PNP, P+PUD, P+P+PNP and P+P+PUD
- Probable Additional value Additional value from the Proved case
- Possible Additional value Additional value from the Proved + Probable
  case

## Calculation Options

The Batch Manager can be used to run economics, creating economic cases
appropriately without creating the reports, or to generate reports from
existing or new economic results.

Recalculation mode:

- Do not calculate (use existing results)
- Calculate if necessary (default)
- Force recalculation

After Calculation:

- Do not show reports
- Show print preview (default)
- Print selected reports
