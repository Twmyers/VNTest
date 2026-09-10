

# Project Options Royalty and Taxes Calculations

- **Book Tax** - The deductible amount is limited to the project or
  entity's available write-off (Taxable Income). Therefore Book Tax can
  never be negative in any year. The distinction between book tax at the
  corporate level only vs on all levels:



- **Corporate level Book Tax** - Used only for corporate taxes. The
  corporate tax paid will never be less than zero, and excess tax over
  taxable income is carried forward only at the corporate level. This
  option uses Current Tax at the entity and folder level, the assumption
  being that negative current tax at the entity and folder level is
  offset by other entities in any time step, but the tax paid at the
  corporate level can never be negative.
- **All-level Book Tax** - The tax treatment is the same in that tax
  paid can never be zero. The difference is that Book Tax is used at all
  levels instead of Current Tax being used at the entity and folder
  level. This does not allow for potential negative tax to be offset by
  other entities in any time step.
- **Current Tax** - The full deductible amount is applied in a time step
  regardless of available taxable income. This allows tax paid to be
  negative, on the assumption that the negative amount will be offset by
  other entities within the corporation that have positive tax payable
  in the same time period. This setting also applies at the corporate
  level, so corporate tax can be negative. Companies may want to use
  this option if there are several tax paying entities within a larger
  tax organization.
