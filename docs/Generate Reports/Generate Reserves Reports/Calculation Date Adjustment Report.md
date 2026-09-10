



# Calculation Date Adjustment Report

Running the Calculation Date Adjustment Report either displays a report
that lists all the entities that may have values that need to be
adjusted after the project has been posted or it filters the project to
those entities. This report should be printed before running a reserves
reconciliation.

Economic data from all relevant reserves categories must be current to
produce accurate results. If economic data is not current when you run a
reserves report,
Value
Navigator runs economics automatically when you run the report.
However, if you want to run reserves economics before running the
reserves report, you must run the *Reserves Options Scenario* on the
**Reports** tab or in the Batch Manager for the entities you want to
report on. If you run the *Reserves Options Scenario* prior to running
reserves reports, the reports automatically detect this and will not run
it again, resulting in faster display of the report. Running the
*Default Scenario* does not necessarily generate the economic results
required to run reserves reports.

See
[Run Economics before Running Reserves Reports](Run%20Economics%20before%20Running%20Reserves%20Reports.md).

To run the Calculation Date Adjustment Report

1.  From the Reserves menu, select Calc. Date Adjustment Report.
2.  Enter the Previous Economic Calculation Start Date.
3.  Do one of the following:
    - Click **Generate Report** to see a report of all entities that may
      need to be adjusted.
    - Click **Filter to Entities** to filter the project to all entities
      that may need to be adjusted.
