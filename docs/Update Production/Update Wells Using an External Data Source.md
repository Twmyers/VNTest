



# Update Production Using an External Data Source

This procedure explains how to update monthly or daily well production
using PPDM (IHS or GeoLogic) or a corporate data hub. Using this method
updates the currently selected wells.

Your External Data Settings in your User Options must be configured
before using the PPDM update, which might require assistance from your
Value
Navigator Administrator.

If you want to update a subset of wells in your project, filter to those
wells first. See
[Flag and Filter Entities](../Filter%20Entities/Flag%20and%20Filter%20Entities.md).

If you want to schedule an update for a later time, or update a subset
of wells based on a well list, see
[Schedule a Production Update](Schedule%20a%20Production%20Update.md) and [Update a Subset of Wells Using a Well List (.txt file)](Update%20a%20Subset%20of%20Wells%20Using%20a%20Well%20List%20txt%20file.md) .

It is highly recommended that you review and understand the [Fit
Settings](../Options/User%20Options/User%20Options%20Forecast%20Settings.md)
and [Import
Parameters](../Options/User%20Options/User%20Options%20Import%20Parameters.md)
in the User Options before importing production data. These settings
affect how data is imported and how forecasts are created in
Value
Navigator.

To update production

1.  Do one of the following: 
    | Select | Description |
    |----|----|
    | File \&gt; Import \&gt; Data Source | When updating from the File menu, you can use the Delay import until option and edit the user, project, and Data Source Import options. |
    | **Entity** \&gt; **Update from External Source**. | When updating from the Entity menu, you cannot use the Delay import until option or edit the user, project, and Data Source Import options.. |
2.  Select your **Data Source** and click **OK**.
3.  Under **Entity Selection**, select the wells you want to update and
    click Next.
4.  (Optional) Edit the user or project options.
5.  Click Finish.

The PPDM update only updates the wells you selected. It doesn't add new
wells.
