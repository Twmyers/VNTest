

# ARIES Import and Export

To import and export ARIES data, you need to install the Access Database
Engine and the AriesDataTools. See
[Install Access Database Engine](Install%20Access%20Database%20Engine.md).

The AriesDataTools can be found in the Aries Converter folder with the
rest of the Val Nav installation files. Your local Val Nav Administrator
or IT department may already have this file stored locally. If required,
you can download the file from the
[Client Portal](https://clients.aucerna.com/)
with the appropriate permissions.

## About ARIES Tools

The tools are targeted to Aries data on US entities. Canadian specific
data may not convert as expected (i.e. royalty interest details,
Canadian capital expense costs (CEE, CDE etc.).

## Export to ARIES

To export to ARIES

1.  Rest at the hierarchy level that corresponds to the entities to be
    exported from
    Value
    Navigator.
2.  Open the Aries Export tool from File
    \&gt; Export \&gt;
    ARIES Project…
3.  Enter a location and file name in the Export
    To field.

The Selection and
Entity Count is updated with the entities
found in the
Value
Navigator database.



### ARIES Scenarios

We export an ARIES ‘case’ per the scenario(s) configured in this area.
The scenarios are based on Plan/ResCat pairs, which define which
Value
Navigator inputs are exported.

In Value
Navigator you can have inputs on PDP and TP (PUD) and on a higher
level economics run, if TP doesn’t exist, we fall back to PDP. This
considers the whole entity, not data area by data area. So in a folder
with mixed entities you get the correct answer at the TP level by adding
the PDP wells in where needed.

In Aries, qualifiers in scenarios are entered in priority order, and
they can be selected area by area, but they don’t ‘fall back’ in the
same way. This lets you run the PDP costs with TP forecast, but it
doesn’t let you insert inputs where some are missing. We couldn’t
reconcile these differences using Aries qualifiers alone so we tried a
different approach.

When you export the TP ResCat in
Value
Navigator, we resolve all ResCat inputs to the TP level and write
out the resolved set to Aries. Then we create the TP scenario in Aries,
which is only intended to tell you what ResCat level the scenario
represents (i.e. there is no priority qualifier behaviour). When you
select the TP scenario you are seeing all
Value
Navigator inputs resolved such that you get the same answer as
what is calculated in
Value
Navigator.

For example:



This logic is extended to all
Value
Navigator plans, so if you have a child ‘Budget’ plan, the inputs
are resolved up the plan chain. So for example, exporting Working/TP and
Budget/TP will get you 2 scenarios in Aries, each of which will give you
the same total resolved result that
Value
Navigator would.

1\. Select Plan and Res Cat combination for the export. Use ‘+ Add Case’
to add additional pairs. The text of the pair defaults to PLAN_RESCAT
but this can be modified by the user.

2\. Select Export to complete the process.

An Aries compatible database (Microsoft Access .mdb) is created in the
location specified in Step 3. The database will contain a single DBSKEY
= ValNavExport

## Import from ARIES

To initiate an import of Aries cases to
Value
Navigator

1.  Open ValNav and create a new, empty project, or connect to an
    existing project.
2.  Launch the Aries import from File \&gt; Import \&gt; ARIES Project…
3.  Specify a path and filename in the ‘ARIES file:’ field. The file
    must be a valid ARIES Microsoft Access .mdb or .accdb database. The
    selected ARIES database must only contain a single DBS key.
4.  Select the ARIES Scenario to import. The list is loaded from the
    selected database file.
5.  Select the ValNav Target plan.
6.  Modify ARIES to ValNav field mappings for Reserves Categories, Well
    Information and/or Production History if required.
7.  Choose a field from AC_PROPERTY that can be mapped to ResCats in
    Value
    Navigator. The field will be added to
    Value
    Navigator Custom Fields for later reference.
8.  Other Aries fields can be mapped to ValNav Custom Fields. The custom
    field will be created and populated on import with the name
    ARIES\_\[Field\].
9.  Select Import to complete the operation.

ARIES scenario qualifiers will be read and used in priority order in the
import.

The Aries field specified as the ValNav Well Name is used to construct
the UWI in ValNav. If there are duplicates in Aries, ValNav appends the
Aries PROPNUM to construct a unique identifier.



## Using the Results

### Export

Create a data connection to the new file and open in Aries.

The scenarios configured in Step 4 above will be available in the
Scenario dropdown in the Explorer. Each scenario contains a single
qualifier of the same name.

Miscellaneous (AC_ECONOMIC Section 2) & Input Settings

### Keywords

LOSS - this is the 'Apply Economic Limit' flag on the Economics General
tab. 'Apply Economic Limit' flag and Economic Limit Calculation type
from Economics section of project options are defined as a LOSS keyword
in Input Settings, Common Lines.

BTU - this keyword is used to modify the GAS phase prices that are
scheduled in a case based on the heating value of the gas. We use this
keyword to export energy content specified on the Declines \| Data
\|Plant tab.
Value
Navigator allows a constant (Default) value and also a date array
for Energy Content. Only default energy content overrides are exported.

SHRINK - this keyword is used to convert produced wet gas into dry sales
gas. We use it to export total gas loss. Just like with energy content,
we export the default total gas loss value if it has an override. Note
that the decimal value that follows the SHRINK keyword is a decimal
factor of dry gas remaining after plant processing (1.00 - total gas
loss).

MAJOR - this is the major phase of a case. In ARIES phase names can only
be 3 characters and are defined in the Eco Streams dialog box (i.e. can
be found in ECOSTREAM table). To be consistent with the three built-in
product lists in
Value
Navigator, we've set up three phase names in the Aries empty
database: oil, gas and cnd.

LIFE - this keyword sets a maximum producing life, based on time, for
the calculations in a case. This feature provides a hard cutoff – no
production will be scheduled beyond this life. This keyword is used to
export the Maximum economic life parameter from the Economics section of
Project Settings.

PW – These lines are used to store the NPV3 and Discount rates found in
the Economics section of Project Settings.

XINVWT – This keyword is used to apply the Chance of Success from the
Economics \| General tab. It risks production and operating expenses.

### Production & Forecasts (AC_ECONOMIC Section 4)

- Production history for the selected entities is exported to AC_PRODUCT
- Complete production forecasts are exported to
  AC_PRODUCT_FORECAST\_\[scenario\] tables as date series volumes. There
  will be a table per scenario.
- Decline expressions are written out in AC_ECONOMIC

The general format for section 4 of AC_ECONOMIC is as follows:

| AC_ECONOMIC |
| --- |
| PROPNUM | SECTION | SEQUENCE | QUALIFIER | KEYWORD | EXPRESSION |
| W0002 | 4 | 1 | WORK_TP | CUMS | 24.015 87.751 |
| W0002 | 4 | 2 | WORK_TP | *START | 9/2016 |
| W0002 | 4 | 3 | WORK_TP | *OIL | 2.29825347 X B/D 6.053684 EXP HAR 7.282108 |
| W0002 | 4 | 4 | WORK_TP | *" | X 1 B/D X YR EXP 6.240547 |
| W0002 | 4 | 5 | WORK_TP | START | 9/2016 |
| W0002 | 4 | 6 | WORK_TP | LOAD | MF1.OIL OIL 9/2016 1/2021 # |
| W0002 | 4 | 7 | WORK_TP | LOAD | MF1.OIL OIL 1/2021 8/2029 #/Y |
| W0002 | 4 | 8 | WORK_TP | START | 9/2016 |
| W0002 | 4 | 9 | WORK_TP | LOAD | MF1.WATER WTR 9/2016 1/2021 # |
| W0002 | 4 | 10 | WORK_TP | LOAD | MF1.WATER WTR 1/2021 8/2029 #/Y |
| W0002 | 4 | 11 | WORK_TP | START | 9/2016 |
| W0002 | 4 | 12 | WORK_TP | GAS/OIL | 6.6686098 X M/B TO LIFE LOG TIME |
| W0002 | 4 | 13 | WORK_TP | *START | 9/2016 |
| W0002 | 4 | 14 | WORK_TP | *CUR/OIL | 0.9823 FRAC TO LIFE |


CUMS is used to specify cumulative oil and gas volume to the start of
the forecast

START is the decline start date in
Value
Navigator

OIL and “ (continuation) are the oil decline Arp’s segment expressions.
These will be commented out (\*) and a LOAD MF1.product… line used
instead based on the following rules:

- A 1+WOR decline: this affects oil volumes and can’t be solved in Aries
- A O+W decline: this affects volumes and can’t be solved in Aries
- When there is both Max Rate and on-time on the
  Value
  Navigator case. We use CUR/xxx for both of these inputs so when
  both are present we have to load the forecast instead.
- When there is a Max Rate on the decline in
  Value
  Navigator that is less than the Qi. In this case the decline
  would not be used in
  Value
  Navigator so we comment it out in Aries and load a flat series
  equal to the Max Rate.
- Ratio decline (e.g. GOR) where Qi and Qf are user entered, Gas will be
  inactive because Aries does not support Arps on ratio declines.
- A manual value in the Wellhead tab cannot be solved for in a formula

LOAD MF#.product… points to the complete, resolved, forecast series in
the AC_PRODUCT_FORECAST\_\[scenario\] tables.

In the example above, Oil is commented out because of a 1+WOR decline in
Value
Navigator.

In the example above, CUR/OIL refers to on-time in the
Value
Navigator forecast.

### Prices (AC_ECONOMIC Section 5)

We are exporting the active
Value
Navigator price deck to a sidefile in Aries. Prices for Oil, Gas,
Cond, NGL, and Sulphur are exported as resolved price streams including
differentials, inflation, and escalation.

We are not exporting price overrides at the well level.

Prices are exported starting from the
Value
Navigator Economic Calculation Start Date in the Economics
section of Project Settings.

Differentials added at the well level in
Value
Navigator are exported as price adjustments in AC_ECONOMIC:

- PRI/OIL xxx
- PAJ/OIL xxx

In the event there are multiple differentials at the
Value
Navigator well level we create references to the product. For
example:

| AC_ECONOMIC |
| --- |
| PROPNUM | SECTION | SEQUENCE | QUALIFIER | KEYWORD | EXPRESSION |
| W000001 | 5 | 1 | WORK_PDP | START | 1/2016 |
| W000001 | 5 | 2 | WORK_PDP | SIDEFILE | BASE_PRICE_SET |
| W000001 | 5 | 3 | WORK_PDP | START | 1/2014 |
| W000001 | 5 | 4 | WORK_PDP | S/195 | -7 X FRAC TO LIFE PLUS 195 |
| W000001 | 5 | 5 | WORK_PDP | START | 1/2014 |
| W000001 | 5 | 6 | WORK_PDP | S/195 | 0.982 X FRAC TO LIFE MUL 195 |
| W000002 | 5 | 1 | WORK_PDP | START | 1/2016 |
| W000002 | 5 | 2 | WORK_PDP | SIDEFILE | BASE_PRICE_SET |
| W000002 | 5 | 3 | WORK_PDP | START | 1/2016 |
| W000002 | 5 | 4 | WORK_PDP | PAJ/OIL | 0.985 X FRAC TO LIFE PC 0 |


In the above example well W000002 has 1 differential in
Value
Navigator so it converts to PAJ/OIL.

- Expenses (AC_ECONOMIC Section 6)
- Ownership (AC_ECONOMIC Section 7)
- Investments (AC_ECONOMIC Section 8)
- Overlays (AC_ECONOMIC Section 9)

### Import

The Aries import creates new entities in the current
Value
Navigator project. There is a new entity for every Aries case
found in the file.

Users can validate inputs using Data Views grids.

We are importing entity level data from Aries AC_ECONOMIC and a limited
number of other tables. Global level Aries inputs such as prices and
escalation schemes are converted as much as possible to the entity level
in Value
Navigator. This means we currently handle only PC and its
variants.

Configuring ownership details in Aries is complex and not consistent
between databases. We try to handle as many keywords and ownership
combinations as we found in sample data and documentation, but resulting
Value
Navigator Interests may not always be an exact conversion.

We are importing a limited number of fields to be imported as Project
Options from the Aries table AC_SETUPDATA. This table can also be used
to store sidefile type data which we are not using in imports.

We are not reading the Aries ECOSTRM table, which includes arithmetic
expressions (i.e. PLUS and MUL in AC_ECONOMICS).

Capital costs in Aries (Investments) are imported as custom costs in
Value
Navigator. Operating costs in Aries have been mapped to
corresponding operating costs in
Value
Navigator.

Capital costs in Aries are imported as Success costs in
Value
Navigator in order to emulate risk in Aries. When risk is
imported as the Chance of Success, the net value of capital calculates
as expected. If there is no risk, then the capital is not affected.

Severance is handled through the tax rate defined on the
Value
Navigator regime as per the price deck.

Aries supports linear calculations for ratios whereas
Value
Navigator only supports Arp’s and other decline equations. When
we convert a non-constant Aries ratio, we convert the ratio values to
override values per time step to preserve product volume results.

Constant NGL/Gas ratios are used as the default NGL ratio in the Plant
tab in Aries. When the Aries NGL/Gas ratio is not constant the last
value will be used as the default.
