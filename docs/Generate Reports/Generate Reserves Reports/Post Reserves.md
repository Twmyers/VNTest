



# Post Reserves

Reserves Reconciliation is performed at the top level of the entity
hierarchy on proved and probable reserves estimates in the Accepted
reserves plan. The current value is equivalent to the opening balance
plus the sum of all changes for all balanced entities. The opening
balance for the next reporting period is the current value less any
value realized during the past reporting period.

Economic cases are evaluated for all entities in the Accepted reserves
plan. Unless all entities are balanced in all Proved and Proved +
Probable reserves categories, the reserves reconciliation will not
proceed. If any entity or any reserves category is not balanced, the
Verify Balance Report will display which entities are not balanced.

Prior to posting the database, generate a report on Company Share, Net,
or Company Share and Net. Once the database is posted, the Economic
Calculation Date will be revised to the Reference Date and values in
this report will not be reproducible without a copy of the database
retained before posting.

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

To post reserves

1.  From the **Reserves** menu, select **Post Reserves**.
2.  Select the jurisdictions.
3.  Select the report options and click **Generate Report** to generate
    the Reconciliation of Reserves report.
4.  Close the Print Preview.
5.  In the **Post Reserves** dialog box, enter the previous post date in
    the From field.
6.  Click **Post Reserves**.



In previous versions of
Value
Navigator, the calculation date moved forward after posting
reserves. In the current version, the calculation date does not move
forward after posting.
