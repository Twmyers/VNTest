



# Copy Reserves Category Input Values within a Well

The Data Manager enables you to copy values for specific tabs from one
reserves category to another within a well. You can do this for several
wells simultaneously.

## Copy Behavior

Technical and economic data is only copied to reserves categories that
already have data. Data is not copied to empty reserves categories even
if you select them. You can override this behavior and copy data to
empty reserves categories by selecting Copy data to target reserves
categories that have no data (see the procedure below). 

In previous versions of
Value
Navigator, the copy behavior described above only applied to
economic data (technical data was always copied to empty reserves
categories). In the current version of
Value
Navigator, this behavior applies to both technical and economic
data.

## Advanced or Basic Copy

You can select Advanced or Basic copy functionality from the context
menu or in the Data Manager dialog box. Basic copy functionality enables
you to copy technical data, economic data or both, but you cannot
specify which technical or economic items to copy. You must copy all
items or none. The advanced copy functionality enables you specify
exactly which technical or economic items you want to copy.

To copy values from one reserves category to another

1.  In the Entity Explorer, select the entity, entities or folder
    containing the wells you want to manage.
2.  From the Entity menu, select **Data Manager**.
    

    You can also access the Data Manager from the Summary window:
    Right-click and select **Copy Reserves Category** (to access basic
    copy functionality) or **Advanced Copy** (to access advanced copy
    functionality).

    
3.  In the **Data Manager** dialog box, select **Copy** or **Advanced
    Copy**, if required.
4.  Select the **Source Reserves Category**. If you are using basic
    copy, the currently selected reserves category is the source. If you
    are using advanced copy, select a reserves category from the
    Reserves Category list.
5.  Under Destinations, select the **Destination Reserves Categories**.
6.  Select or deselect **Apply** to children of groups.
7.  Select the Items to **Copy**.
8.  If you are using Advanced Copy, for each Cost, Interest, and Price
    Differential you select under **Items to Copy**, select an option
    from the Options column. The table below describes costs, but the
    descriptions also apply to interests and price differentials.
    | Option | Behaviour |
    |----|----|
    | Replace All | All costs in the destination entity are deleted. Selected costs are copied to the destination entity. |
    | Replace Selected | All costs in the destination entity that match the selected costs are deleted. Selected costs are copied to the destination entity. Other costs in the destination entity are retained. |
    | Append New | All costs in the destination entity are retained. All selected costs are copied to the destination entity. New costs that correspond to existing costs are appended with a modified name (a number is added to the new cost name). This function enables you to copy duplicate costs. |
9.  Select any of the following options, as required (advanced copy
    only):
    | Option | Description |
    |----|----|
    | Copy data to target reserves categories that have no inputs | Forces the copying of data to empty reserves categories.  |
    | Delete copied items from source | Deletes selected items from the source reserves category. |
    | Delete copied items from all non-Common reserves categories | Only enabled if Common is selected as the destination reserves category. All data for the selected **Items to Copy** are deleted from all reserves categories other than Common. |
10. Click **OK**.
