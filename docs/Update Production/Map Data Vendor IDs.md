



# Map Data Vendor IDs

The Vendor IDs dialog box is used to map data vendor well IDs to wells
in your project. Mapping data vendor IDs to wells enables the following:

- Updating wells from multiple data vendors even though each vendor may
  have a different ID for the same well,
- Using custom names for wells even though data vendors do not recognize
  those names
- Matching well codes in daily data with UWIDs in a project

When a well is first imported into a
Value
Navigator project, its UWID (Unique Well Identifier) or API Field
ID is used as the UWID for the project. However, you can assign other
IDs used by different data vendors to that well in the Vendor IDs dialog
box. Once another data vendor’s ID has been assigned to a well, the well
can be updated from that source.



An entity’s Vendor ID or API is displayed in the Properties Window
(under Identification) in the bottom left of the screen when you select
the **Properties** tab.



Daily data sources do not contain well codes instead of UWIDs. Before
importing daily production, you must map the codes and the well UWIDs.

To map a new vendor ID to a well

1.  In the Entity Explorer select the entity or folder level of entities
    you want to add vendor IDs to.
2.  From the **Administration** menu, select **Vendor IDs**. The Vendor
    IDs dialog box displays the current entity or all entities in the
    folder selected in the Explorer. \&gt;
3.  If the vendor you want to use is not displayed in the Vendor IDs
    dialog box, right-click in any column header to display the Show
    Columns dialog box.
4.  Select the vendors you want to use for mapping and click **OK**.
5.  Enter the vendor IDs in the appropriate row and column.
6.  Click **OK**.
