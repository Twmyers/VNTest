



# Rename an Entity

When you rename an entity, keep in mind that:

- Entity names are not case sensitive. Therefore, a name such as **NEW
  WELL** cannot be used if the name **New Well** is already in use.
- Renamed entities retain their globally unique identifier. Data
  associated with the well does not change when you rename it.
  Value
  Navigator will continue to treat the renamed well as if it was
  the original well. This behaviour can affect the merging of projects.
  See [Merge Projects](../../Importing%20and%20Exporting/Merge%20Projects.md) for more details.
- You can use the name of a deleted entity, but doing so links the
  renamed entity with the deleted entity’s reserve reconciliation
  records (applies only to wells and only in a posted database).
- The deleted entity’s Vendor ID remains linked to the renamed entity
  unless you select **Delete associated Vendor IDs** in the **Rename
  Entity** dialog box. Using the correct vendor ID is required for PPDM
  production updates. For more information, see
  [Map Data Vendor IDs](../../Update%20Production/Map%20Data%20Vendor%20IDs.md).

## Rename a Single Entity

To rename a single entity

1.  In the Entity Explorer, right-click the entity you want to rename
    and click **Rename Entity**.
2.  Enter a new name.
3.  Select **Delete** **associated Vendor IDs**, if required, and click
    **OK**.

## Rename Several Entities

To rename several entities

1.  From the Entity menu, select **Rename Entities**.
2.  In the **Batch Rename** dialog box, enter the Old UWI and the New
    UWI for all entities you want to rename. You can also import a .txt
    or .csv file by clicking **Import**.
3.  Select **Delete** **associated Vendor IDs**, if required, and click
    **OK**.
