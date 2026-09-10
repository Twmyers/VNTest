



# Schedule a Production Update

This procedure explains how to schedule a PPDM (IHS or GeoLogic) or
daily data production update. Once you schedule an update, you cannot
use Value
Navigator until the update is complete.
Value
Navigator must remain running until the update is complete.

It is highly recommended that you review and understand the [Fit
Settings](../Options/User%20Options/User%20Options%20Forecast%20Settings.md)
and [Import
Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md)
in the User Options before importing production data. These settings
affect how data is imported and how forecasts are created in
Value
Navigator.

## Tagging Updated Wells

When you update production, you can tag the updated wells with text
(using a custom field) so you can identify the updated wells after the
update. See the procedure below for details.

To schedule a production update

1.  From the **File** menu, select **Import**.
2.  In the Import dialog box, select **Import from data source(s)** and
    select the data sources you want to use.
3.  Do one of the following:
    | If | Then |
    |----|----|
    | You want to update wells based on a well list, | **A**.  Under Wells to Update, select **Well List**. **B**.  Browse to the well list text file and click **Open**.  |
    | You **do** **not** want to update wells based on a well list, | **A**.  Under Wells to Update, select the wells you want to update. |
4.  Click **Next**.
5.  If required, edit the **Import Options** by clicking **Edit**.
6.  Do one of the following:
    | If                                                | Go to       |
    |---------------------------------------------------|-------------|
    | You want to tag the updated wells,                | Step **7**. |
    | You **do** **not** want to tag the updated wells, | Step **9**. |
7.  Select the custom field from the **Populate Custom Field** list.
8.  Next to the **Populate Custom Field** list, type the text you want
    to appear in the custom field of the imported wells.
9.  Click **Next**.
10. If necessary, edit the **Data Source Import Options**.
11. Click **Finish**.\
    A countdown to the update is displayed.
12. If you want to override the update delay and import now, click
    **Import Now**. If you want to cancel the scheduled import, click
    **Cancel**.

You must leave
Value
Navigator running until the update is complete. The wells are
updated on the specified date according to the Import Parameters and
External Data Settings in .

If you entered text in a custom field, you can find the wells with that
text on **Wells and General Economics \| Well Info** **and Custom
Fields**.
