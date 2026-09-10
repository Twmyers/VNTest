



# Merge Projects

Merging Value
Navigator projects can involve exporting data (using an XML file)
from two or more projects, importing that data into a project that
already has data, or importing that data into an empty
Value
Navigator project.

See [Export Project Data](Export%20Data/Export%20Project%20Data.md) for more details on export
behavior.

When merging projects, there are several factors you need to consider,
some of which might involve editing the data before exporting it.



[Entity Hierarchies](#)



If the hierarchies in the projects to be merged are edited versions of
the Default hierarchy, when you import the XML files into your new
project, the hierarchy of the last imported file is applied to the
project. Other Default hierarchies are not imported.

If the hierarchies in the projects to be merged are custom hierarchies
(not edited versions of the Default hierarchy), all *Project*
hierarchies are imported into the new project. *User* hierarchies are
not included in exports and not imported into new projects.

If the projects to be merged have different hierarchies, but you want
all the wells to fit into the same hierarchy, you will have to edit one
or both hierarchies and any Custom Fields used to create them before
exporting them.

See [Create or Edit an Entity Hierarchy](../Entity%20Management/View%20and%20Organize%20Entities/Create%20or%20Edit%20an%20Entity%20Hierarchy.md) .







[Project Options](#)



If the Project Options are not the same in the projects to be merged,
the results in the merged project might be different than they were in
the original projects.

Before merging projects, determine which Project Options you want to use
in the merged project and then use one of the following approaches:

- Configure the project options in the destination (new) project before
  importing any data and ensure Project
  Options is *not* included in any of the exported files.
- Determine which of the projects to be merged has the Project Options
  you want to use. Include the Project Options when exporting that
  project’s data, but do not include Project Options for any other
  exports.





## Price Decks

Determine which price decks you want to use in the merged project. When
exporting data from the projects you intend to merge, only select the
price decks you intend to use. Ensure you activate the correct price
deck in the merged project.



If you merge files that have price decks with the same names, but
different prices, the price deck imported last will overwrite the
previously imported version.



## Companies

If the projects you intend to merge contain different companies,
consider whether you want those companies added to the entities in the
other projects once they are merged.

By default, companies are always included in new interests. Therefore,
if you import new wells into a project that contains Company A, that
company will automatically be added to the Interests of the imported
entities. To prevent companies from being added to imported wells, go to
the **Companies** dialog box (**Tools** \&gt; **Global Project Data** \&gt;
**Companies**) in all the files to be merged and deselect **Include in
new entity interest**

See [Add a Company to the Project](../Entering%20Economics/Set%20Up%20Interests%20and%20Royalties/Add%20a%20Company%20to%20the%20Project.md).

## Entity Names

If the projects to be merged have entities with the same Display Names,
those wells in the source project will have
(from import) appended to their Display names, unless you
deselected Include Project IDs in the Export dialog box when you
performed the export, in which case the source wells will overwrite the
destination wells.

Renamed entities retain their globally unique identifier. Data
associated with the well does not change when you rename it.
Value
Navigator will continue to treat the renamed well as if it was
the original well. This behaviour can affect the merging of projects.
See [Rename an Entity](../Entity%20Management/Create%20and%20Edit%20Wells/Rename%20an%20Entity.md).

If any project has any renamed entities that originally had the same
name as the entities in any of the other projects to be merged,
Value
Navigator will interpret those renamed wells as being the same
wells (because renamed wells retain their globally unique identifier
(Object ID), which you cannot view or edit). The entities imported last
will overwrite any previously imported entities. You can

and [Object IDs vs. Display Name](Export%20Data/Export%20Project%20Data.md#Object) .

To merge Value
Navigator projects

1.  Export data from the project you want to merge by going to the
    **File** menu and selecting **Export** \&gt; **File**.
2.  In the **Export** dialog box, determine the Entity Data, Price
    Decks, Advanced Options, and Project Data you want to export. \&gt;
    

    The items you select might exist in the other projects you intend to
    merge and the selections might conflict with each other. See the
    *Entity Hierarchy*, *Project Options*, *Price Decks*, *Companies*,
    and *Entity Names* sections below for more details.

    
3.  Save the exported file as an XML file.
4.  Repeat steps 1-3 for any other files you intend to merge.
5.  Either open a project that already has data or create a new, empty
    project to serve as the destination for the data you exported in
    steps 1-4.
6.  Import the XML file you created in steps 1-3 by going to the
    **File** menu and selecting **Import** \&gt; **File**.
7.  Browse to the first file and click **Open**.
8.  If you need to edit User or Project Options click **Edit**.
9.  Click **Next** to finish the import.
10. Import any other files into the merged project.



If the imported files contain conflicting data, data in the last
imported file will overwrite data from the previously imported files.
