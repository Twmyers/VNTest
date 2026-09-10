

# Decisions Overview

The Decisions feature helps teams bridge the gap between asset
development and economic evaluation. It enables companies to define the
key economic drivers that shape evaluation results—such as development
area, completion design, and lateral length—and apply those drivers
consistently across their well inventory.

By using Decisions, evaluators can:

- Distill complex inputs into manageable choices that reflect how wells
  are developed and generate economic results
- Build and compare development scenarios based on meaningful variations
  in these choices
- Rapidly update large well inventories with planned development
  assumptions, without manually adjusting underlying economics for each
  well

For example, a decision like Completion Design can determine which
capital model is applied, while a decision like Lateral Length can scale
drilling costs accordingly. Together, these decisions create a flexible
structure for modeling what-if scenarios or aligning asset economics
with current development plans.

## Lookup Matching & Scaling

At the core of the Decisions feature is a powerful mechanism for
aligning well-level assumptions with economic inputs: lookup matching
and scaling.

In Val Nav, capital and operating cost lookups can be configured to
represent specific development choices—such as Completion Design or
Development Area—by associating each with one or more Decision values.
When a well is modeled with a matching set of Decisions, Val Nav
automatically applies the corresponding lookup, ensuring inputs reflect
the selected development plan without manual intervention.

In addition to categorical matching, lookups can incorporate scaling
based on numeric Decisions, such as Lateral Length. This allows users to
express inputs not as fixed values, but as functions of a development
driver. For example, drilling costs can be set to scale linearly with
lateral length.

This dual capability—matching for categorical variation and scaling for
numeric flexibility—gives users a structured yet dynamic way to
represent the economic impact of development decisions at scale.

## Defining Decisions at the Project Level

Decisions are defined at the project level, meaning they are shared
across your entire well inventory to ensure consistency and reusability.
While Val Nav provides a set of default Decisions out of the box, these
can be customized or replaced to align with your company’s naming
conventions, development strategies, or asset-specific drivers.

There are two types of Decisions:

- Text Decisions: Represent categorical choices (e.g., Completion
  Design). These must be defined as a controlled list of
  options—free-form text is not allowed, as strict matching is essential
  for automation and lookup selection.
- Numeric Decisions: Represent continuous values (e.g., Lateral Length).
  These require a unit type to ensure proper handling of Imperial/Metric
  conversions.

Decisions are configured through Tools \&gt; Global Project Data \&gt;
Decisions.

&gt; ⚠️ Important: Decisions cannot be deleted if they are referenced
&gt; anywhere in the project—whether by wells, scenarios, or economic
&gt; lookups. This prevents accidental loss of critical configuration and
&gt; ensures model integrity.

This centralized configuration model allows teams to align on a
consistent set of development drivers while giving them the flexibility
to tailor those drivers to specific evaluation needs.

## Characterizing Lookups through Decisions

The core to enable this functionality is characterizing both the wells
and the lookups with these decisions. First, lookups: Val Nav allows
users to characterize capital and operating cost lookups with Decisions,
determining how lookups are matched and scaled to each well.

#### Matching on Text Decisions

Text Decisions are applied at the lookup definition level, meaning the
same settings apply across all decks that use the lookup. These
Decisions define how a particular lookup matches:

- Decisions not explicitly set on the lookup are ignored during
  matching.
- If a lookup has no Decisions defined, it cannot be matched.
- So, a match occurs only when each Decision assigned to a lookup
  exactly match those defined on the well, ignoring any other decisions.

#### Scaling from Numeric Decisions

Within each lookup, scalars can be set for individual cost entries.
Allowing each cost to use a different scalar enables flexible cost
modeling. For example, drilling costs may scale linearly with Lateral
Length, while gathering costs remain fixed.

Today, all numeric decisions are options to apply as linear scalars.
Framing scaling as a scalar optoin in lookups with linear numeric
decisions scaling as an option maintains a pathway to support more
sophisticated multi-variate, non-linear scaling in the future.

#### Configuring Lookups with Decisions

Lookup characterization can be performed:

- Directly through the Val Nav UI
- In bulk using the Capital and Operating Cost Deck import functionality

## Modeling Wells & Groups

To implement Decision-based behavior at the well level , two components
must be configured:

1.  The Decision values must be assigned to the well
2.  The relevant data area must be set to use the new Lookup Matching
    mode.

When both are set, Val Nav can automatically apply the correct lookup
based on matching Decision values. Even when not matched, lookups can
still be scaled based on numeric Decisions if those scalars are defined.

#### Inventory Tab: A Unified View

The new Inventory tab consolidates the Schedule and Decisions data
areas, while preserving their independent rescat inheritance. Within
this tab:

- A dedicated pane displays which lookups would be matched for each data
  area, based on the current Decisions.
- A ✔️ or ❌ icon appears next to each data area to indicate whether it
  is in lookup matching mode.
- Since multiple lookups can be assigned to a data area, multiple
  lookups can be matched simultaneously.

#### Lookup Matching Mode

Lookup matching mode is a new, explicit input mode alongside Manual and
Lookup modes. Input mode is no longer implied by the existence of data:
it must be explicitly set.

#### Bulk Assignment Tools

Both Decision values and input modes can be updated using Val Nav’s
comprehensive bulk editing tools, including the Data View, Spreadsheet
Import, Input Copier, and Data Manager.

This flexibility allows users to assign and update Decisions efficiently
across thousands of wells, ensuring consistent application of economic
assumptions with minimal manual effort.

## Reconciliation & Decisions

Decisions can play a key role in the reconciliation process,
particularly when evaluating how changes in development plans impact
economic results.

#### Option to Disconnect Lookups on Promotion

A project-level option gives you the option to realize assumptions
driven by lookups on promotion into manual inputs. This can simplify
Reserves review and reconciliation by breaking wells connections to
lookups, preventing future changes to them from affecting reserves in
the review process.

When disabled, the link to lookups is preserved throughout the reserves
workflow, allowing evaluations to remain sensitive to evolving lookup
assumptions.

#### The Decisions Step in Reconciliation

As part of the reconciliation process, Val Nav introduces a dedicated
Decisions step, which covers:

- Changes to Decision definitions (e.g., new options, renaming,
  reconfiguration)
- Updates to Decision assignments on individual wells

This step does not reflect changes to the underlying lookup models
themselves. Those changes are tracked within the Capital and Operating
Cost reconciliation steps.

This frames the Decisions step as capturing changes to how a well is
characterized, while lookup updates represent changes to the assumptions
behind those characterizations.

Together, this separation provides clarity and precision when tracking
the impact of both development plan changes and evolving economic
assumptions.
