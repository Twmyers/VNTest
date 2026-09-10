

# Behind-pipe Scheduling Tool

This tool reschedules wells based on the economic limit of other wells.
Each completion is modeled as a separate well. The tool finds the wells
based on a specified custom field and determines the schedule - through
either technical rates or economic limits - and updates the wells
accordingly.



If you modify the wells or update your price deck, you will have to
re-run the tool to recalculate the schedule.





As this tool looks at the major reserves category, you can have a mix of
PDP, PD, and TP variants on the wells. PDPs will never be rescheduled
(they’ve already happened).

The tool will detect multiple rescats on the same well and schedule them
in this order: PDP, PD, TP. Incremental-mode workover forecasts will be
detected and rescheduled, but we recommend against using them for this
work flow.

If you choose to carry different schedules in 1P, 2P, and 3P, beware of
the use of the Project Start field outside of this tool (including the
**Timeline** tab). Using the regular tools in
Value
Navigator, parallel rescats always shift by the same amount,
which will break the sequences determined by this tool.

When a single well is selected when the tool is invoked, only that
well’s linkages will be scheduled. For folder selections, all unique
‘wellbores’ in the selection will be considered, including wells that
may not be in the current folder.

The economics are always run outside of any shared calculation (common
termination or ring fence) so as not to unduly burden each individual
well.

The completion delay applies to the well it is entered on (i.e., it is
redundant on the first well in sequence, which will not be rescheduled).
The delay must be a time-based custom field. You can therefore specify a
delay in either months or days (the use of hours or years is not
supported).

## Transition Method

When transitioning from one completion in a wellbore to another, the
Behind-Pipe Scheduling Tool can use either and **Economic limit** or
**Production forecast threshold**.

The **Economic limit** calculates economics for each well completion in
the sequence, determines when it becomes uneconomic, and then starts the
next well at that date (plus any delay).

The **Production forecast threshold** causes a well transition based on
a technical rate, which can be more stable, as the transition is not
based on price. Use this option to input thresholds for oil vs. gas
wells, in the appropriate units (i.e., when completion is producing 5
bbl/d or less). The wells will transition when their primary monthly
producing rate is below the threshold.

To use the tool:

1.  On Wells and General Economics \| Well Info
    and Custom Fields, [create three custom fields](../Entity%20Management/View%20and%20Organize%20Entities/Configure%20Custom%20Fields.md):
    1.  A text field for grouping wells together (e.g., ‘Wellbore’). You
        can also use an existing text field if appropriate.
    2.  A numeric field for specifying the sequence
    3.  A numeric field, with unit type = time, for specifying the
        completion delay

    
2.  Using the Data Views \| Well Info & Custom
    Fields view, populate the above fields with values for your
    wells.
3.  In the Entity Hierarchy, select the well(s) or folder you want to
    reschedule.
4.  From the Tools menu, select
    Behind Pipe Scheduling.
5.  Complete the following options:
    | Option | Description |
    |----|----|
    | Wellbore identifier | Select the first custom field you populated in step one. |
    | Sequence | Select the second custom field you populated in step one. |
    | Completions Delay | Select the third custom field you populated in step one. |
    | Scenario | Select a [scenario](../Generate%20Reports/Use%20the%20Batch%20Manager/Create%20and%20Run%20a%20Scenario.md). |
    | Schedule based on | Major reserves category to run. |
    | Schedule only within proved | Only affects the specified reserves category. |
    | Synchronize timing for parallel reserves categories | Synchronizes timing for parallel reserves categories. If you carry 1P, 2P and 3P forecasts, do you want timing kept in sync? |
    | Transition Based On | Select either Economic Limit or Production Forecase Threshold. If **Production Forecase Threshold** is selected, input the threshold rate in the appropriate field, for either Oil or Gas. |
6.  Click Reschedule to run economics and
    reschedule the wells.
