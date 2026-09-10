

# Rename Reserves Categories

To rename reserves categories

1.  Go to Tools \&gt;
    Global Project Data \&gt;
    Reserves Categories.
2.  Edit the Abbreviation and/or
    Name.
3.  Click OK.

## Queries Affected by the Ability to Rename Reserves Categories

With the ability to rename reserves categories, the reserves category
names formerly stored in the CODE_LOOKUP table are no longer used, and
those rows will be deleted on upgrade. Queries referencing the
RESERVE_CATEGORY code type in that table will need to be rewritten to
instead join on the FISC_RESERVE_CATEGORY table.
