



# Break-even Analysis Behaviour

## Prices in the Break-even Analysis



For the purpose of performing the BEA, prices, entities, overrides, and
differentials are altered as described below. These changes are
performed on copies of the entities and prices. The changes are not
saved in the database. Only the calculation results are saved.



The active price deck and entities (as they are loaded) are flattened
and all overrides and differentials after the reference date are
removed. General inflation overrides are also flattened. Prices are set
up with overrides at the reference date (or before if that value
continues sparsely) to be factored by adding a % differential. This
means that prices that only have differentials from parent prices are
not themselves factored but change as a result of their relation to the
parent factoring. For each iteration, each of these prices is factored
by the same amount. Resulting entity prices and benchmark prices can
then be pulled directly and reported.

Since the NPV changes depending on product price and on par and
reference pricing, the analysis scales par and reference prices
simultaneously. Royalty prices scaled include:

- Alberta ISC Reference prices
- Alberta Par prices
- Alberta Reference prices
- Alberta Transportation adjustments
- Alberta WTI Royalty price
- British Columbia PMP prices
- Saskatchewan Par prices
- Saskatchewan provincial gas price (PGP)
- The BEA does not scale:
- British Columbia Gas Select price
- British Columbia Oil Threshold prices
- Saskatchewan Gas Cost Allowance
- Pricing Units

The units displayed for product prices when displaying BEA results can
vary depending on whether you are resting on a well, or on a folder, and
whether you are the analysis on a single entity (Break-even tab) or on
multiple entities (**Comparison** tab).

On the **Break-even** tab, the entity currency is always be honoured.
When generating folder-level results, the project currency is always be
used.

On the **Comparison** tab, results are displayed on each entity in the
folder. If all entities within a folder are using the same currency,
then the entity results and the folder results will be run using the
same currency.

The units displayed for benchmark prices depend on the units used for
the benchmark itself within the price deck.

## Break-even on a Single Entity

On a single entity, the steps for determining break-even are:

- All product prices at the reference date are flattened for the life of
  the well
- The selected options are used
- The process begins by factoring the product price or prices (starting
  at 100%) to determine the NPV value
- Depending on the nearness to NPV = 0, a new factor is chosen
- All prices are factored by this new factor, again determining the NPV
- Factoring continues until NPV = 0 is achieved. This is the break-even
  price.

When determining the break-even price, there is a \$500 tolerance on the
resulting NPV, which means the analysis stops running further iterations
once the resulting NPV is within \$500 plus or minus zero. This is to
prevent the same break-even results from appearing multiple times as the
NPV reaches zero. 

If the resulting NPV reaches zero exactly, the analysis continues to
iterate until it finds a positive NPV that is within a 0.1% factor of
the closest zero result. The analysis does this because an NPV = 0
probably indicates that the case has gone uneconomic at that price and
so it needs to continue to look for the exact price at which the case
reaches NPV = 0.

## Break-even on a Folder

When running break-even analysis on a folder, there are two different
types of results: consolidated folder results (Break-even tab) or
individual entity results (Comparison tab).

On a folder, steps for determining a consolidated break-even are:

- Take all product prices for each entity within the folder at the
  reference date and flatten these prices for the life of the entities
- The process begins by factoring the product price or prices for each
  entity (starting at 100%) to determine the NPV value for each entity
  at that factored price
- The resulting NPVs for each entity within the folder are summed into a
  consolidated NPV
- Depending on the nearness to NPV = 0, a new factor is selected
- All prices for each entity are then factored by this new factor, again
  determining the NPV for each individual entity, again summing the
  results into a consolidated NPV for the folder
- Factoring continues until a summed or consolidated NPV reaches 0. This
  is the break-even price for the consolidated folder.

Since entities within a folder can possibly have differing prices, it is
essential to select a Benchmark price when running a consolidated BEA on
a folder in order to bring the break-even price back to a common
denominator.

On a folder, steps for running the individual entity results are similar
to determining break-even on a single entity, as noted above.

## Economic Limit Behaviour

When running a break-even analysis, you can choose to honour or ignore
the economic limit setting on the entity. 

When running a BEA, the economic limit always applies to cash flow, so
the option to apply the economic limit to net operating income or before
tax cash flow is not relevant.

Honouring an economic limit means that you are finding a break-even
price—a price below which the entity becomes uneconomic to operate.

Ignoring the economic limit allows a break-even price to be calculated
assuming that the well would run out to its technical limit, and that
all costs to that point will be considered for determining the lowest
price at which the maximum volume can be economically produced from the
well.

## Break-even on a Common Termination Entity

A BEA can only be run on a Common Termination Entity (CTE) while in the
CTE view. Running a BEA on a CTE is similar to running a folder
consolidation, which looks for the price at which the summed total of
all NPVs of the child entities reaches zero. 

While running break-even for a CTE, the common termination date is
re-calculated with all child entity prices flattened and factored, for
each iteration. If you have entered a Manual Termination date, then this
date is considered, and the iterations are run within this constraint. 

CTE entities have logic of their own, in that you can choose to honour
or ignore the economic limit of the child wells and of the CTE itself.
Since there is a setting in the BEA to honour or ignore the economic
limit settings on an entity or a folder, the CTE should be treated
similar to an entity.

- **Break-even on a child entity of a CTE\**
  Running a BEA on a child entity of a CTE is different than a normal
  entity. The analysis does not try to find when NPV reaches zero.
  Instead, it runs the full CTE break-even analysis including all child
  entities and cost entities in order to find the break-even factor.
  Then, using that factor, it runs the child entity results and reports
  that as the break-even price.
- **Break-even on a folder that contains a child entity of a CTE\**
  The BEA runs like a normal folder consolidation, but for each
  iteration a common termination date is calculated for any CTE entities
  and this is used to calculate the NPV.
