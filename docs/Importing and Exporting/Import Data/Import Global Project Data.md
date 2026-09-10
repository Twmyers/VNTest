

# Import Global Project Data

The Global Project Data import is a full-cycle workflow to mass create
or update it via Excel. Currently, it is limited to Price, Capital Cost,
and Operating Cost Decks.

Due to its exacting data model with many dependent data areas, an exact
template is required for imports. The template is populated with all
current data to:

- Guide you on the required format and dependent data
- Enable you to bulk update the data already in place

On import, validation will inform you about all errors and warnings
found. Always address errors from preceding sheets first.

Remember: Global project data imports, like all global project data
changes, should be made in a locked project with no other users in the
system.

Price, capital cost, and operating cost decks have the most dependent
data, so it is critical to understand the right merge/replace/replace
option for your use.

## Merge/Replace/Replace All – Overview

Below the Merge/Replace/Replace All options are detailed for cost and
price decks separately. Generally, these refer to how data not in the
import file is handled by the import. All data in the import file is
always honored verbatim, including creating any objects that previously
did not exist in the Val Nav project. The exception are decks, which
must be created from the UI.

Please see the user stories and examples for each of the options
separately for price and cost decks below:

## Merge/Replace/Replace All – Cost Decks

For Cost Decks, the key consideration is what you want to happen to:

- Lookup-Deck pairs in the project but not in the import file
- Costs in the project on Lookup-Deck pairs that exist in the import
  file but not in the import file.

In all cases where a cost within a lookup-deck is being updated, the
entire date array is fully replaced with the new assumptions in the
spreadsheet.

### Merge

"I want to provide a partial update of some lookups in some subset of
decks I care about. I don't want to change anything about other lookups
or decks. I also don't want to change anything about other costs within
the lookup-deck pairs that I'm importing."

Example: I'm updating the drilling cost within the Permian lookups for
the Reserves deck only. I don't want to change Bakken lookups. I don't
want to change the asset team’s LRP decks. I also don't want to change
the completion costs within the Permian-reserves deck either.

### Replace

"I want to provide a full update of some lookups in some subset of decks
I care about. I don't want to change anything about other lookup or
other decks. I do want to fully replace all costs the within the
lookup-deck pairs that I'm importing."

Example: I'm updating all costs within the Permian lookups for the
Reserves deck only. I don't want to change Bakken lookups. I don't want
to change the asset team’s LRP decks. I do want to change the drilling
and completion costs within the Permian-reserves deck.

### Replace All

"I want to provide a full update of all lookups in all decks I care
about. I want to fully replace everything in the project with what is in
my import file. If the lookup doesn’t exist in my import file at all, I
want to delete it. If a lookup exists but a lookup-deck pair doesn’t, I
want to wipe the lookup for that deck. Effectively, everything not in
the import file will be deleted, if allowed, or completely wiped. This
is the most drastic option.



You cannot delete decks through an import, so decks won’t be deleted.



Example: I'm updating the entire view of costs in the project. I’m
updating lookups for all assets and all decks and all costs within those
lookup-deck pairs. Those that aren’t in my file are either deleted or
wiped.

## Merge/Replace/Replace All Options – Price Decks

Extending this thinking to price decks, there are a few differences to
consider:

It is not an exact match because we don't have the lookup concept of
multiple costs within a singular lookup. You cannot update a few prices
within a lookup of prices and need to consider whether to remove those
other prices or leave them alone. For this reason, merge and replace are
effectively the same. So, the primary consideration for price decks is
what you want to happen to:

- Price or other fiscal components (e.g., royalty prices, tax rates,
  inflation rates, etc.) in the project but not in the import file

In all cases, where a price or fiscal component is being updated, the
entire date array is fully replaced with the new assumptions in the
spreadsheet. Further, it’s expected to provide a full view of a price
instance including all differentials and overrides within the deck being
imported. There is no equivalent partial update of components to a
price.

### Merge or Replace

"I want to provide a full update of some stream prices in some subset of
decks I care about. I don't want to change anything about other stream
prices or other decks."

Example: I’m only updating WTI and Henry Hub in the Reserves deck. I
don’t want to change Louisiana Light Sweet. I don’t want to change WTI
and Henry Hub in LRP decks.

### Replace All

"I want to provide a full update of all stream prices and all decks. I
want the only information to exist to change anything about other stream
prices or other decks.

Example: I'm updating the entire view of prices and fiscal data in the
project. I’m updating all price and fiscal projections across all decks.
Those that aren’t in my file are either deleted or wiped.
