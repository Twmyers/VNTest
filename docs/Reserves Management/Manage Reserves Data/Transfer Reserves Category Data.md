

# Transfer Reserves Category Data

The Category Transfer tool simplifies the process of copying a well from
one reserves category to another (from PUD to PDP, for example).

The tool:

- Transfers the entity from one reserves category to another and removes
  the inputs from the source category
- Creates a change record for the transfer
- Creates a change record for the revisions
- Balances the entity before or after the transfer, depending on the
  option you select

## Entity Selection

You can use the tool on single or multiple entities, folders, ring
fences (RF), or common termination entities (CTE).

For multi-entity selections, the tool doesn’t transfer entities that
don’t have data in the source reserves category. It will still balance
those entities, per the option selected.

For CTEs and ring fences, you should run the category transfer on the
entire CTE or RF. This ensures the entire shared calculation is
balanced, as the transfer may impact economic results on un-transferred
wells.

To transfer entities

1.  In the entity hierarchy, select the entity. entities (using
    CTRL + click or
    SHIFT + click), or the folder you
    want to reconcile.
2.  Go to one of the locations below and click
    Category Transfer:
    1.  Change Management menu
    2.  Entity menu \&gt; Data Manager
    3.  Summary window (right-click)
3.  Select the following options:

| Option | Description |
| --- | --- |
| Transfer | Select the source and destination reserves categories. |
| Source | Select the source reserves category. |
| Destination | Select the destination reserves category. |
| Transfer Category | Select a change record category for the transfer. |
| Revision Category | Select a change record category for entity revisions. |
| Mode | Select a mode: Balance, then transfer: Revisions are made in the original res cat before transferring. Balances the original reserves category and captures the current balance as a transfer record. Transfer, then balance: Revisions are made in the destination res cat. Captures the opening balance as a transfer record, then balances in the destination to capture revisions. |
| Apply to children of groups | Include or exclude the children of groups. |


1.  Click **Transfer** or **Transfer and Close**.
