



# Copy Input to other Entities

The Input Copier enables you to copy data from one entity to others in
several reserves categories or from one reserves category to another in
the same entity. Set up all of the economic parameters which will be
common to a number of wells on a single well, in Entity View. Then copy
those parameters can then to all wells with like economic parameters.

Bulk editing tools are also available using the Data View grids and most
information stored in
Value
Navigator can be imported in bulk with a spreadsheet import.
Security permissions are required to use some of the bulk editing tools.
Contact your administrator for access.

Technical and economic data is only copied to reserves categories that
already have data. Data is not copied to empty reserves categories even
if you select them. You can override this behavior and copy data to
empty reserves categories by selecting Copy data
to target reserves categories that have no inputs (see the
procedure below). 

In previous versions of
Value
Navigator, the copy behavior described above only applied to
economic data (technical data was always copied to empty reserves
categories). In the current version of
Value
Navigator, this behavior applies to both technical and economic
data.



A Project Start date on the source reserves category is not copied using
the Input Copier.



You can simplify the selection of destination wells in the Input Copier
by [filtering](../../Filter%20Entities/Filtering%20Overview.md) to them
first.

To copy data

1.  From the Explorer, select the source well, reserves plan, and
    reserves category.
2.  From the **Tools** menu, select **Input Copier**.
3.  Select an Items to Copy option:
    | Option | Behaviour |
    |----|----|
    | Resolved | Copies data (whether input override or inherited) from the source to the same plans and reserves categories in the destination entities. **Note:** The override/inherited state from the source well replaces the state on destination well(s). |
    | Direct | Copies input overrides that are entered directly on the source plan and reserves category (not inherited data) to the destination. |
4.  Specify the Destination Entities.
    

    Filtering to the destination wells before opening the Input Copier
    causes only those wells to appear under the Destination Entities.

    
5.  Specify the **Destination Reserves Categories** and **Plans** (only
    available if you selected **Direct** in Step 3).
    

    You can select all **Reserves Categories**, but data will only be
    copied to categories that already have data. Data is not copied to
    empty reserves categories. However, you can copy data to empty
    reserves categories in step 7, if required.

    
6.  Select the **Items to Copy**. Black items exist in the Source. Grey
    items do not exist in the Source. You can expand items to select
    sub-items)
7.  If required, select **Copy data to target reserves categories that
    have no inputs**.\
    This option copies data to empty reserves categories.
8.  Click **OK** to copy.

Use the Auto-play feature (see
[Play Through Wells](../View%20and%20Organize%20Entities/Play%20through%20Wells.md)) to automatically scroll
through the list of wells in the Entity Explorer while viewing the
results in the various Prices & Costs
tabs to validate the results of the Input Copier. Don’t forget to
clear your filter when you have finished verifying .

## Copying Liquid Production

When copying liquid production ratios and efficiencies, data is copied
to the destination well regardless of whether the source or destination
has a Plant Gas Analysis. Copying ratios always creates a product stream
where there is gas production. Copying efficiencies only creates a
product stream in destination wells that have a Plant Gas Analysis.
