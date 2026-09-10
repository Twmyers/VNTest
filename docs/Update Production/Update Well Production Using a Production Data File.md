



# Update Production Using a Production Data File

This procedure explains how to update wells with a production data file
you exported from a data vendor, such as Accumap.

It is highly recommended that you review and understand the [Fit Settings](../Options/User%20Options/User%20Options%20Forecast%20Settings.md) and [Import Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md) in
the User Options before importing production data. These settings affect
how data is imported and how forecasts are created in
Value
Navigator.

To update production using a production data file

1.  Export the data in
    Value
    Navigator format from the vendor’s system and save to your
    local drive or a network location.
2.  On the **File** menu, click **Import**.
3.  Select **Import from existing file**.
4.  Browse to the production data file and click **Next**.
5.  If you need to edit the Import Options, click **Edit**.
6.  Click **Next**.
7.  Select the appropriate current month.
8.  Click **Finish**.

If the file contains wells that aren’t in your project, those wells will
be imported. If auto-forecasts are enabled,
Value
Navigator will generate forecasts for any *new* wells. Forecasts
on existing wells are not updated.
