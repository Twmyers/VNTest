

# 2021 v2 Release Notes

## New Features

### Spreadsheet Import of Comments

Comments can now be imported from Excel or CSV via the new mapping
option in the Spreadsheet Importer. So whether comments are generated
from another source or a legacy system, they can be brought into Val
Nav's Info tab and graph comments. When importing graph comments, you
can specify the color and the series or date they attach to. As always,
the import mapping template guides you to possible mappings and their
options and requirements.



### Database Merging via XML Export

To facilitate better communication of data across a company that
supports multiple databases for the same wells, XML exports can now be
set to exclude object IDs with a toggle on the export dialog menu. This
forces the merging upon import to be done based on a UWI/Display Name
basis instead of Object IDs, which are auto-generated IDs not editable
nor even available from the interface. This offers a simpler and less
stringent option for sharing Val Nav data across projects.



### Scatterplot

You can now plot well performance metrics directly against completion
parameters to help understand the relationship between completion
designs and performance. You can now easily answer questions such as:

- What kind of relationship does lateral length have with EUR?
- Does increasing proppant or fluid explain variance in EUR at higher
  lateral lengths?
- Does reducing cluster spacing accelerate production in the first 12
  months?



On a new Scatterplot tab on the Cross Plot tab, you set both X and Y
axis variables to any numeric well attribute or any calculated
performance indicator, such as EUR and peak rate. These variables are
available in shared dialog options with the other Cross Plot side tabs
so analysis can be carried across to the other statistical plots. Now
that two variables are set, the other tabs plot each of their
distributions as opposed to the old behavior where one distribution was
always fixed to EUR.

### Colour Cross Plot Graphs by Attributes

With the creation of the scatterplot, Val Nav 2021 v2 also has the
ability to colour the plot by any text-based attribute. This has been
extended to all other cross plot tabs except the Frequency chart, which
can't be coloured per well. This addition enables you to extend your
analysis with qualitative data like completion style, target formation,
well spacing, and much more. Work was also done to strive for
consistency of colours of the same attribute across different sample
sets.



### Enhanced Cross Plot Graph Interactions

The Cross Plot can now display relationships and outliers so you can
select, review, and adjust them to ensure quality data is used
throughout Val Nav's holistic type well process.

We have also added more fidelity in interacting with the plots via
keyboard shortcuts that enable simple selection and deselection of
wells. The following keyboard shortcuts are now available in the graphs:

- CTRL+drag inverts a selection of wells
-  SHIFT+drag extends a selection
- CTRL+SHIFT+drag selects wells within
  the drag bounds and deselects outside the bounds

With this new functionality, you can filter to the selected wells or use
them to generate a type well. Other new functionality includes:

- Selecting individual wells from a point on the new cross plot or the
  data grid
- Accessing a well on the Declines tab directly from the Cross Plot tabs
  using the Open in Declines Tab option



### Break-even Analysis on Wedges

The break-even tool has now been extended to calculate on wedges. Now
you can analyze the break-even of projects defined by their incremental
contribution, like re-fracs, workovers, and facility expansions. Whether
the wedge is input directly or derived by subtraction, the calculator
can iterate prices to solve for the break-even point with a simple
selection of the wedge from the Reserves Category dropdown. The
breakeven tolerance was also revised for more precise answers,
especially in cases where the economic limit is honoured.



## Other Enhancements

- Extended the Merge Plan tool to work on Ring Fence entities
- Added two new cross plot variables that calculate cumulative volumes
  from either monthly or daily volumes
- Updated Cross Plot report to include the new scatterplot and colour
  functionality
- Updated how the normalization field is stored in the database. It is
  now a double instead of string.
- Changed the install location from *Energy Navigator* to *Quorum
  Software*

## Bug Fixes

- Fixed an issue where the economic limit delay field was not working
  properly on uneconomic, undeveloped reserves categories.
- Fixed an issue on the Entity Price Forecast report where Val Nav
  incorrectly showed an economic calculation banner.
- Fixed an issue where normalization of certain fields did not calculate
  correctly outside of the three base plans: Working, Pending, and
  Accepted.
- Fixed an issue on hierarchy report tables where the first year of
  after tax data was ignored when a mid-year reference date was used.
- Fixed a deadlock issue with automated reconciliation of ring fence
  entities.
- Fixed an issue where Excel spreadsheets couldn't be generated form
  Data Views while another Excel copy was open.
- Fixed a logging issue where vendor IDs warning messages were
  excessively recorded.
- Fixed an issue where wells modified by the Val Nav integration service
  will no longer
  delete(Undefined
  variable: General.Aucerna Execute)vendor IDs.
- Fixed an issue where the Bulk Well Generator updated forecast starts
  when Apply Source Changes was off.
- Fixed an issue where type well normalization couldn't be applied to
  some custom plans.
- Fixed an issue where unit magnitudes weren't retained in cross plot
  table.
