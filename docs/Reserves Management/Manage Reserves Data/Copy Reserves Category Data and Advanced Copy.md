



# Copy Reserves Category Data (and Advanced Copy)

The Data Manager enables you to copy values for specific tabs from one
reserves category to another within an entity. You can do this for
several entities simultaneously.

## Copy Behaviour

Technical and economic data is only copied to reserves categories that
already have data. Data is not copied to empty reserves categories even
if you select them. You can override this behaviour and copy data to
empty reserves categories by selecting **Copy data to target reserves
categories that have no data** (only in the Advanced Copy). 

In previous versions of
Value
Navigator, the copy behaviour described above only applied to
economic data (technical data was always copied to empty reserves
categories). In the current version of
Value
Navigator, this behaviour applies to both technical and economic
data.

If a Project Start date exists on the source Reserves Category it will
be copied to other non-PDP categories.  Project Start is not copied to
PDP, P+PDP, or P+P+PDP.

## Advanced or Basic Copy

Basic copy functionality enables you to copy technical data, economic
data or both, but you cannot specify which technical or economic items
to copy. You must copy all items or none. The advanced copy
functionality enables you select specific technical or economic items.



Data from the source category *replaces* data in the destination
category. The data is not *appended*.



To copy data for several entities, do one of the following first:

- Select the entities in the Entity Explorer (using the **Shift** key to
  select consecutive entities or the **Ctrl** key to select
  non-consecutive entities)
- Select the folder level of the entities you want to copy
- [Flag and Filter Entities](../../Filter%20Entities/Flag%20and%20Filter%20Entities.md)

## Basic Copy

To copy general forecast or economic reserves category data

1.  In the Entity Explorer, select the entities you want to modify.
2.  Select the plan and reserves category you want to copy data from.
3.  From the **Entity** menu, select **Data Manager** and click **Copy
    Reserves Category**.
    

    You can also access the **Data Manager** from the **Summary**
    window: Right-click and select **Copy Reserves Category**.

    
4.  Under **Destination**, select the destination reserves category or
    categories.
5.  Under **Items to copy**, select the items you want to copy.
6.  Click **Copy** or **Copy and Close**.

## Advanced Copy

To copy specific technical or economic reserves category data

1.  In the Entity Explorer, select the entities you want to modify.
2.  Select the plan and reserves category you want to copy data from.
3.  From the **Entity** menu, select **Data Manager** and click
    **Advanced Copy**.
    

    You can also access the Data Manager from the Summary window:
    Right-click and select **Advanced Copy**.

    
4.  Select the source reserves category from the Reserves category list.
5.  Under **Destination(s)**, select the destination reserves category
    or categories.
6.  Under **Items to copy**, select the items you want to copy.
7.  Under **Options**, select the following options, as required:
    | Option | Description |
    |----|----|
    | Copy data to target reserves categories that have no inputs | Forces data to be copied to destination reserves categories with no inputs. |
    | Delete copied items from source | Selected items are deleted from the source reserves categories. |
    | Delete copied items from all non-Common reserves categories | Selected items are deleted from all source reserves categories, except Common. |
8.  Click **Copy** or **Copy and Close**.
