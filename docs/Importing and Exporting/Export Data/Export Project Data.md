



# Export Project Data

Use this procedure to export any of the following items:

| Price Decks Batch Definitions Change Record Categories Companies Company Logo Countries Currencies Custom Data Fields Fiscal Regimes Facilities Hierarchies Meter Stations | Prices, Royalties, Tax Rates, and Price Sets Project Options Scenarios Summary Types (Change Record Category Summaries) Tax Pools Transportation Area Bulk Well Schedules Rollups Type Wells Wells and Groups Security Plans |
| --- | --- |


Also see
[Export a Well List](Export%20a%20Well%20List.md) ,
[Export Project Options](Export%20Project%20Options.md), and
[Export User Options](Export%20User%20Options.md).



If you are exporting entities for the purpose of importing them into
another Value
Navigator project, see
[Merge Projects](../Merge%20Projects.md)
for important guidelines.



We recommend reading the expandable sections below for important details
before exporting project data.



[Dependencies in the Export List](#)



Some items in the Data to export list are dependent on other items. For
example, if you select Batch Definitions,
Hierarchies is also selected because
Batch Definitions are based on a hierarchy. Likewise, Price Decks are
dependent on Prices, Royalties, Tax Rates & Price Sets, Countries, and
Currencies. If you deselect Currency, for
example, Price Decks is deselected
automatically because you cannot export a Price Decks without
currencies.







[Parent and Child Entities](#)



When you export a parent entity (an entity that contains other wells,
such as a group, rollup, bulk well schedule or a type well) its children
are automatically included in the export.

If you export a well that is a child of a parent entity (such as well
used to create a type well), the parent is not automatically exported.







[Default Project Options File](#)



If you are creating a default project data file, deselect all options
that you do not want to include in the file. Usually, you will only want
to include the **Project Options** and the desired **Project Data**
selections. However if you want the same price deck used in all new
projects, ensure you include it in your export.







[Price Decks](#)



All price decks in the project will be selected by default. To manage
file size, deselect any price decks not required for the export. If you
are exporting Scenarios, make sure the Price Decks used in the Scenarios
are selected to include them in the export.







[Advanced Options](#)



Batch Definitions will be merged with any already existing if your data
is subsequently imported into another project.

Project Options and Security Settings will replace the settings in any
project that your data is subsequently imported into.







[Project Data](#)



All Project Data options are selected by default. Use caution when
deselecting Project Data options to ensure that no dependencies are
violated.







[Entity Selection](#)



Entity Selection determines how Linked Entities are exported.

- All Entities will include all linked entities (such as wells linked to
  type wells or bulk well schedules) in the export and the links between
  them are maintained.
- Filtered Entities will include entities related to the filtered
  entities according to the Entity Data selections in the export.
- Current Selection exports only the selected entities. Entities linked
  to the selected entities are not exported.

The export will default to All Entities. If you have filtered your well
list, Value
Navigator will automatically select the Filtered Entities option.
Ensure that any linked entities required in your export are included in
your filter or selected in the Entity Data section.







[Reserves Data](#)



If you want to export a copy of a posted database that will allow you to
change the economic calculation start date, ensure that
Include change records and opening balances
is NOT selected.







[#](#)[Object IDs vs. Display Name](#) 



In Value
Navigator all entities have an underlying Object ID, which
uniquely identifies that entity independently of its regulatory name
(UWI or API number, for example) or user-assigned name (Display Name as
seen in the Entity Explorer). The Object ID is automatically assigned to
entities by
Value
Navigator and is not accessible in the user interface. The Object
ID enables an entity's data to be associated with it even if its
original name is changed.

Object IDs are important when It also prevents an entity from
overwriting another entity with the same name when imported from another
project.

The difference between Object IDs and entity names becomes important
when you want to merge data for a well from one project into another
project with the same well. If the source and destination projects both
contain a well called Well A,
Value
Navigator will not necessarily consider those the same wells even
though their names are the same. If the wells were created in separate
projects, their Object IDs will not be the same despite the identical
well name and their data will not be merged upon import. In most cases,
this behaviour is beneficial but there might be cases where you want
Value
Navigator to consider two wells with identical user-assigned
names to be the same well. In that case, you need to
deselect Include Object identifiers in
the Export to File dialog box when
exporting data from the source project. When you deselect this option,
Value
Navigator uses the Well Name instead of the Object ID to identify
entities.





## Export Project Data

To export project data

1.  If required,
    [filter](../../Filter%20Entities/Filter%20Entities%20Overview.md)
    to the entities you want to export.
2.  Select **File** \&gt; **Export** \&gt;
    File.
3.  In the **Data to Export** list, select the data you want to export.
4.  If you are exporting entities, select the wells you want to export
    (under **Entity Selection**).
5.  Under **Wells and Groups**, select **All** **data** or **Forecasts
    only**.
    

    The **Forecasts only** option is intended to export forecasts
    (Declines/Wellhead information only, not Plant Gas Properties) to an
    XML file which should be imported into projects where the same wells
    already exist. On import, existing forecasts will be completely
    replaced by the forecasts in the matching wells in the XML file. No
    other well data is included in the exported XML file, so it should
    not be used to create new wells.

    
6.  Choose whether to include change records and opening balances.
7.  Select the Plans to include in the export.
8.  In the **File** name field, click ![](../../Images/Export-Project-Data-1.jpg).
9.  Type a name for the file and browse to a location to save it.
10. Click Save and then click **OK**.
    

    Selecting Compress File converts the
    .xml file into a
    Value
    Navigator-specific file, which can only be opened in
    Value
    Navigator.

    
