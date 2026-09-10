



# Configure Custom Fields

Custom Fields are optional fields used to label entities with text,
dates or numbers and are displayed in Data View. Custom Fields are
available to all entities in a database and apply only to the entity
where data has been entered. By default, the custom fields will be
visible on the Wells and General Economics \|
Well Info and Custom Fields grid, but you can create your own
grid to display only Custom Fields. You can use custom fields to:

Custom Fields are used to label wells with text, dates or numbers. You
can then use the custom fields to:

- Identify new wells imported into a project (using the Import Tag,
  below)
- Create a custom entity hierarchy (see
  [Create or Edit an Entity Hierarchy](Create%20or%20Edit%20an%20Entity%20Hierarchy.md) )
- Filter to wells (see
  [Create a Filter Query](../../Filter%20Entities/Create%20a%20Filter%20Query.md)
- Assign view and edit rights to users
- Specify an IP rate that you can select on the Cross Plot Report
- Enter a working interest factor for working interest roll ups

To create a custom field

1.  Do one of the following:
    1.  On the Wells and General Economics \|
        Well Info and Custom Fields (in the **Data View)**, click
        **Edit Custom Fields**.
    2.  In the **Tools** menu, select **Global Project Data** \&gt;
        **Custom Fields**.



1.  In the **Custom Fields** dialog box, click **Add** in the bottom
    left corner.
2.  Click Add and enter a name for the
    custom field.
3.  Select one of the Field Types and complete the options.
4.  Click OK.
5.  Complete the options below, as required:
    | Option | Description |
    |----|----|
    | Requires administrative privilege to edit values | If you select this option, users must have the *Modify Custom Fields* policy in their security settings to edit the custom field. |
    | Enforce list validation | If you add selectable values to the custom field (see below), this option enforces the selection of those values only. Users cannot enter free text values in the custom field. |
6.  **Optional**. To add selectable values for the custom field, click
    **Add** under the Definition area of
    the **Custom Fields** dialog box.
    

    If the project contains text values in the custom field already,
    click Update list values to
    automatically add the text values to the list.

    
7.  Under **Select Default List Value for New Entities**, select the
    value you want to use as the default for new entities, if required.
8.  Click **OK**.

To export custom fields for use in another project, see [Export Project Data](../../Importing%20and%20Exporting/Export%20Data/Export%20Project%20Data.md).

To import custom fields exported from another project, see [Import Project Data](../../Importing%20and%20Exporting/Import%20Data/Import%20Project%20Data.md).
