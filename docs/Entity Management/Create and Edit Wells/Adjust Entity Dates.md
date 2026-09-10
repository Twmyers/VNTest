



# Adjust Entity Dates

The Adjust Dates dialog box is a planning tool used to move entity dates
forward or backward in time. You can adjust the dates for items such as
declines, costs, interests and royalties, and entity start dates. Adjust
Dates is useful for adjusting the dates of wells in a drilling program
because it maintains the relative time relationships between the wells. 

When you adjust the forecast, it is transposed to the adjusted date
(rather than extrapolated). Its parameters (such as its initial rate,
decline rate, etc.) are not altered.



If the forecast starts before the Current Month, it is extrapolated to
the Current Month and then transposed after that.



## Relative Date Adjustment

This option moves all entities by the same relative amount. Declines
move by day. All other dates move by month only. Custom field dates will
move to the same date in the relative month.

## Absolute Date Adjustment

This adjustment moves all entities to a common date based on an anchor
type: first forecast date or first capital date. When multiple entities
are included in the selection, the entity (or entities) with the
earliest forecast date or capital date is moved to the new absolute
date.

All other wells in the selection are moved the same relative amount.
This maintains offsets between wells.

## Reserves Categories Selection

By default, All Except Developed Producing and Common, is selected. This
allows you to adjust only non-producing reserves categories. To adjust
well level data (entity fields, production history, etc.), you must
select All Reserves Categories under Options. When you select All
Reserves Categories, the options under All Reserves Categories in the
Items to Adjust section become active.

To adjust the dates on an entity or folder

1.  In the entity explorer, select the entities (or folder level) you
    want to adjust. Filter to the entities first, if required.
2.  From the **Entity** menu, select Adjust Dates.
3.  Under Adjustment Date Setup, select **Relative** or **Absolute** and
    enter the time adjustment amount or date.
4.  Under **Options**, select one of the following:
    | Option | Description |
    |----|----|
    | All Reserves Categories | Adjusts dates for all reserves categories and enables you to adjust the options under All Reserves Categories. |
    | All except Developed Producing and Common | Adjusts only non-producing categories. Common is not adjusted. |
    | Current Reserves Category | The reserves category you currently have selected. Only data that is not being inherited from another category or plan is moved. |
5.  If you do not want to apply the adjustment to the children of
    groups, deselect **Apply to children of groups**.
6.  Under **Items to Adjust**, select the items you want to adjust.
7.  If you selected **All Reserves Categories** in step 4, the items
    under **All Reserves Categories** are active. Select the items you
    want to adjust.
8.  Click **OK**.
