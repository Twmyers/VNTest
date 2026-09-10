

# Specify a Change Reason on Wells

Change Reasons act as a Change Record Category override in the automated
reserves reconciliation (ARR) process. For example, if you acquire a
well, you might want to log all changes to the well under the
Acquisition change record category, even if the changes you make (such
as forecast revisions or price changes) would not normally be associated
with that change record category. To do this, you specify a Change
Reason on the well.

There are two types of Change Reason: Change Reason (Entity) and Change
Reason (Detail):

- **Change Reason (Entity)**: Any change record created uses the Change
  Reason as the change record category, regardless of the type of
  change.
- **Change Reason (Detail)**: Any change that falls under a Summary Type
  is assigned the specified Change Reason (detail). For example, you
  might have several change record categories (including one called
  Advanced Technology) that all fall under the Summary Type “Technical
  Revision”. If you specify Advanced Technology as the Change Reason
  (Detail), any type of change that would fall under Technical Revision
  is given a change record with Advanced Technology as the change record
  category.



Only use one change reason type at a time. If you specify both types of
change reason, the detail change reason is ignored.



## Change Reasons on New Wells

All wells require an opening balance or a Change Reason to use the ARR
process. When you create a new well, it has no opening balance so you
must specify a change reason. Without an opening balance,
Value
Navigator cannot determine the type of change you’ve made, so it
uses the Change Reason.

Once you post your database, your new entities will have an opening
balance so you no longer need the change reason. You can continue to use
it or delete it from your wells. To delete change reasons in bulk, go to
the Data View, **Wells and General Economics \| Well Info and Custom
Fields**.

You can specify a Change Reason in three places, as described below.

## Well Information Dialog Box

To specify a Change Reason in Well Information

1.  In the entity hierarchy, right-click the well and select **Edit
    Entity**.
2.  In the Well Information dialog box, select the **Reserves
    Properties** tab.
3.  Select a **Change Reason** (Entity and/or Detail).
4.  Click **OK**.

## Data View

To specify a Change Reason in Data View

1.  In the main toolbar, select **Data View**.
2.  Select **Wells and General Economics \| Well Info and Custom
    Fields**.
3.  Scroll to the Change Reason columns (far right).
4.  Select a **Change Reason** (Entity and/or Detail).
5.  Click **Save** in the Data View.

## Predictions \| Declines

To specify a Change Reason on **Predictions \| Declines**

1.  Go to **Predictions \| Declines** and click (far right).
2.  Under Quick Display Fields, either change an existing field to
    Change Reason or add a field and select **Change Reason**.
3.  Click anywhere outside the dialog box to close it.
4.  In the display field above the decline parameters, select the
    **Change Reason**.
