



# Spreadsheet Creation Guidelines

Whether you are using an existing spreadsheet or creating a new
spreadsheet based on a spreadsheet import template, there are several
critical factors to consider:

- If you are creating your own spreadsheet, create column headings using
  Value
  Navigator terminology. When you open the spreadsheet in the
  Spreadsheet Import tool,
  Value
  Navigator will attempt to detect the type of data you are
  importing and configure the import column headings. However you should
  still confirm that column headings are correctly configured before
  importing.
- Create Sheets to hold different sets of data rather than creating
  separate files. Creating Sheets will enable you to create import tasks
  more efficiently because you can work from a single file rather than
  using several files.
- Group data for the same well together. For example, if you have
  capital costs for Well 1 on three dates, create three consecutive rows
  for Well 1. There can be no intervening rows of data.
- Organize data in the order it should be entered in the user interface.
  This is important in cases where entering a value causes another value
  to be recalculated. When in doubt, first try entering values in the
  user interface to determine the order required to achieve the desired
  results. The importance of order is also relevant when importing
  several import tasks at the same time. See
  [Create Spreadsheet Import Tasks](Create%20Spreadsheet%20Import%20Tasks.md).

## Tips

- To exclude data in the spreadsheet from the import without deleting
  it, hide the columns or rows.
- [Generate a Spreadsheet Import Template](Generate%20a%20Spreadsheet%20Import%20Template.md) by
  clicking ![](../../Images/Spreadsheet-Creation-Guidelines-1.png) in the Spreadsheet Import tool (after
  selecting a Mapping type).

## Warnings

- Importing empty columns or rows for fields that already have data in
  your project will overwrite the existing data with a null value.
- The Import Operations (Merge, Replace, and Replace All) in the
  Spreadsheet Import tool affect whether project data is overwritten or
  deleted. The Import Operations behavior depends on the data mapping
  type you are working with. Before selecting an Import Operation,
  carefully read the tool tip for each operation by placing your mouse
  pointer over the operation.
