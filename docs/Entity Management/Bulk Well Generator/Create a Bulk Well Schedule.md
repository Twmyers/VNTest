



# Create a Bulk Well Schedule

To create a well schedule, you use a well or wells as the source for all
the wells in the schedule. The well you use as the source should have a
forecast (including gas analysis and products if applicable), interests
and royalties, a chance of success (COS) and a chance of occurrence
(COO). You can also add Allowances or Volumetrics (both are optional).

When a well is created from a Bulk Well Generator in a non-PDP reserves
category, the Project Start will automatically be created and set to the
Start Date.

## Production Start Date

By default, the date used for start of production on each well in the
schedule is equal to the amount of time between the last capital
expenditure and the start of production in the source well.

You can override the default start of production date with a common
production start date. The common production start date on
Bulk Well Generator \| Definition applies
to all wells in the row. See the procedure below for more details.

To create a well schedule

1.  In the Explorer, right click the source well, point to **Create
    as,** and select **Bulk Well Generator**. (You can specify other
    source wells once you have created the schedule).
2.  In the Create Bulk Well Generator dialog box, type a name for the
    schedule.
3.  Enter Entity Properties information, if required.
4.  Enter text for the Custom Fields, if required (to organize the wells
    into a folder in the Entity Hierarchy).
5.  Click **OK** to create the schedule.\
    The new schedule appears in the Explorer.
6.  Select the new schedule in the Explorer and go to **Bulk Well
    Generator \| Definition**. The source well appears in the first row
    of the schedule.
7.  Complete the following fields:
    | Field | Description |
| --- | --- |
| # of Wells | The number of wells you plan to drill. |
| # of Rigs | Number of available rigs. Determines how long it will take to drill the number of wells you indicated based on the time you enter in Time Between Wells. Example: If you indicate two wells and one rig with 30 days between wells, the second well will be drilled 30 days after the first. If you indicate two wells and two rigs, both rigs will be drilled on the same date. |
| Start Date | First capital expenditure date. |
| &lt;link&gt; | Link to previous date (optional). Not used in the first line of the schedule. If selected, drilling of the wells in this line will not begin until the final well in the previous line has been drilled. The first available date after the previous well has been drilled is used automatically. |
| Last Start Date | First capital expenditure date of the last well in the line. Example: If you indicate Start Date of January 1, 2011 for two wells and one rig, and a Time Between Wells of 30 days, the start date of the last well will be January 31, 2011. |
| Time Between Wells (unit) | The days or months between wells. You can change the unit by selecting Days or Months in the bottom right corner of the screen. |
| Common Production Start Date | Date on which all wells in the row will begin producing. Entering a date overrides the default first production date. See Production Start Date above. |
| COS , COO, Production, and Capital Factors | Reduces or increases the COS, COO, Production, or Capital Costs for the wells in the line. |

8.  Click **Add**, to add a row, if required.
9.  Select a different source well, if required, by clicking in the
    **Source Well** field and selecting a well from the list.
10. Repeat steps 7 to 9, as required.
11. To view the schedule, click the **Timetable** tab.
