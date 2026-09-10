



# Create a Well

If you are working in a corporate database, your rights to see wells
might be limited. In this case, copying a well might be preferable to
creating a new one because the new well might not be visible to you
unless you enter the required Custom Field data. See *Cautions for
Creating New Wells in a Corporate Database* below.

Also see
[Copy an Entity](Copy%20an%20Entity.md)
and [Edit Entity Information](Edit%20Entity%20Information.md).

To create a new oil or gas well

1.  In the Entity Explorer, right-click, point to **Create**, and select
    **Oil Well** or **Gas Well**.
2.  In the **Well Information** dialog box, complete the following
    fields, as required:
    | Tab | Field | Description |
| --- | --- | --- |
| Well Properties | Display Name | Name displayed in the Entity Explorer. |
| Well Name | Well Name |
| Field | Field |
| Field Code | Field Code |
| Pool | Pool |
| Pool Code | Pool Code |
| Country | Select the country. See Add a Country. |
| State/Province | Select the Province or State. See Add a Province or State. |
| County/District | County/District |
| Operator | Operator |
| Licensee | Licensee |
| Unit | Unit |
| Status | Status |
| Well Type | Oil Gas Water Source Solvent Injection Gas Injection Water Injection Cost Entity Undefined |
| Product List | Oil, Gas, or Condensate |
| Entity Currency | Select the currency for economic calculations. See Add a Currency. |
| Well Profile Type | Deviated Horizontal Slant Vertical |
| Surface Lat/Long | Horizontal wells are displayed on the map with a square to indicate the surface location with a line leading to the bottomhole location. SeeView Horizontal Deviation on the Map. |
| Bottomhole Lat/Long |
| Parent Entity | Optional. Add the new entity to a Group, Rollup, Type Well, Common Termination Entity, or Ring Fence. |
| Reserves Properties | Oil Reserves Type | Standards of disclosure for oil and gas require that products be designated by the type of material being extracted and reserves reports are displayed according to these product types. Select the appropriate oil and gas reserves types. Light and medium oil Heavy oil Bitumen Synthetic oil Shale oil Tight oil |
| Gas Reserves Type | Gas Shale gas Coal bed methane Hydrates Solution gas Synthetic gas |
| Custom Fields | Import Tag | A field used to label wells with custom information. See Configure Custom Fields |

3.  Enter appropriate values on the Custom
    Fields tab to sort your new wells into Entity Hierarchy
    folders.
4.  Ensure the Country and
    State/Province fields are populated.
    Economics are based on the location of the wells.
5.  Click **OK**.

## Create Wells on the Map

You can also point to a location on the Map tab and create a well. The
Latitude and Longitude of your mouse pointer position are displayed at
the bottom left of the map.

To create a well on the map

1.  Click the **Map** tab.
2.  Move your cursor to the location on the map where you want to create
    the well.
3.  Right-click and click **Create Oil Well** or **Create Gas Well**.
4.  Enter the **Display Name** (this is the name that appears in the
    Entity Explorer), Well Name, Field, and Pool.
5.  Select the **Country**.\
    If the country you want to use is not displayed,
    see[Add a Country](../../Countries%20and%20Currencies/Add%20a%20Country.md) .
6.  Select the **Province** or **State**.\
    You must select the country before this list is populated.
7.  Select the **Entity Currency**.\
    For more information on selecting the entity currency, [Set the Entity Currency](../../Countries%20and%20Currencies/Set%20the%20Entity%20Currency.md).
8.  Enter the remaining well information, as required, and click **OK**.

## Cautions for Creating New Entities in a Corporate Database

If you are a user with limited viewing and editing privileges creating a
new well, type well, or group in a corporate database, you must enter
the appropriate text in a Custom Field in order for the entity to be
visible because your user rights are based on the Custom Fields. If your
user rights to see entities are limited by Custom Fields and this
information is not entered for the new entity, the entity will not be
visible to you. If you are about to create an entity that will not be
visible to you, a warning is displayed.

Copying a well, rather than creating a new one, automatically populates
the well information and attributes (including Custom Field
information). The copied well will appear in the same folder as the
source well whereas newly created wells go to the bottom of the Entity
Explorer unless their well information and attributes are entered.
However, it is important to remember that factors such as volumetrics,
gas analysis, plant products and pressures are also copied.

If you have created a new well, but cannot see it, contact your
administrator and ask to have the appropriate Custom Field information
entered for the new well.
