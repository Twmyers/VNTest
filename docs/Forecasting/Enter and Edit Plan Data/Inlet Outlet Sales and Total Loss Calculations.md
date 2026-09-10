



# Inlet, Outlet, Sales, and Total Loss Calculations

The Inlet Gas Volume, Outlet Gas Volume, Sales Gas Volume, and Total
Loss displayed on **Predictions \| Data** are calculated as shown below:

- Inlet Gas Volume = Raw Gas \* (1 – Surface Loss)
- Outlet Gas Volume = Plant Inlet \* (1 – Processing Loss)
- Sales Gas Volume= Plant Outlet \* (1 – Fuel Loss)
- Total Loss = 1 – (Total Sales/Total Raw)

## Enter Surface, Process, or Fuel Loss on the Plant Tab

### Enter Surface Loss

You can enter Surface Loss at three levels: the project-level default,
well-level default, and well-level monthly. See the table below for a
description of each surface loss type and where to enter the value.

| Surface Loss Type | Location | Behaviour |
|----|----|----|
| Project default | **Tools \&gt; Options \&gt; Project Options** | All wells in the project use this value. You can override the value on each well. |
| Well Default | **Predictions \| Data \| Plant**, in the blue **Default** row of the Surface Loss column | Overrides the project default. The value is applied to all months in the forecast. You can override the monthly value by entering a value in the data grid. |
| Monthly | **Predictions \| Data \| Plant**, in the Surface Loss column | Overrides the well default. When you enter a value for a month, that value is applied to subsequent months in the forecast (but you can also override them). The entered value is displayed with a grey background to indicate it is an override. |

### Enter Process Loss or Fuel Loss

You can enter Process Loss or Fuel Loss at two levels: the well-level
default and well-level monthly. See the table below for a description of
each process loss type and where to enter the value.

Process Loss is automatically calculated when you enter a volume, rate,
efficiency, or ratio for any NGL product. You can override the
calculated number.



You can only enter **Process Loss** on the **Plant** tab when you select
the **Raw** or **Inlet** input modes. See
[Select an Input Mode on the Plant Tab](Select%20an%20Input%20Mode%20on%20the%20Plant%20Tab.md).



| Process or Fuel Loss Type | Location | Behaviour |
|----|----|----|
| Well Default | **Predictions \| Data \| Plant**, in the blue **Default** row of the Process Loss or Fuel Loss columns | The value is applied to all months in the forecast. You can override the value by entering a value in the data grid. |
| Monthly | **Predictions \| Data \| Plant**, in the Process Loss or Fuel Loss columns | Overrides the well default. When you enter a value for a month, that value is applied to subsequent months in the forecast (but you can also override them). The entered value is displayed with a grey background to indicate it is an override. |

### Default Process Loss with CO2 and H2S

H2S and CO2 are removed from the gas stream according to the following
logic:

- If CO2 \ (the [CO2 Allowable](../../Options/Project%20Options/Project%20Options%20General.md) set
  in project options), then CO2 is removed from the gas stream, down to
  CO2 Allowable, resulting in a process loss.
- If H2S \&gt; 0, then all of the H2S is removed from the gas stream,
  resulting in a process loss.

### Enter Volumes, Rates, Ratios or Efficiencies on the Plant Tab

To enter Natural Gas Liquid (C2-C5+), NGL or Condensate data, such as
monthly volume, calendar day rate, or ratio, go to **Predictions \|Data
\| Plant**.

For Ratios or Efficiencies, you can enter a Default or Monthly value.
For Volumes or Rates you can only enter Monthly values.

### Entering or Changing a Ratio or Efficiency

- In the grid view of dates and product yields, enter a rate, volume,
  ratio or efficiency at any date to adjust the yield. Only one type of
  override can exist for any product. In other words, you cannot enter
  ratios for one year, and then volumes for the next year.
- When you enter a rate, volume, or ratio, the cell background turns
  grey to indicate an entered value.
- When you enter a rate, the volume is automatically calculated and
  displayed with a grey background. (The opposite is true when you enter
  a volume.) The calculated ratio or volume is displayed in grey text to
  indicate it is based on the entered rate or volume.
- When you enter a ratio, the value is automatically applied to all
  subsequent months. (You can still edit values for the subsequent
  months.) Volumes and rates are automatically calculated and displayed
  in grey text to indicate they are based on the entered ratio.
- Process Loss and Energy Content are automatically recalculated, but
  they can be overridden by entering values. To enter an NGL or
  Condensate volume, rate, or ratio, one of these columns must be in
  view, as they cannot be calculated using an Efficiency.
