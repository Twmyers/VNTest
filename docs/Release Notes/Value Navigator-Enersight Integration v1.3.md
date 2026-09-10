

# Value Navigator-Enersight Integration v1.3

- Added the ability to import operating costs from Enersight against raw
  gas. Requires Enersight 2.15.
- Added the ability to map to the new Copy Asset From If New flag in
  Enersight 2.15, to allow additional templating on well creation. Use
  the mapping item "CopyAssetFromIfNew".
- Added the ability to use SAML logins to connect to Enersighwt.
- Added the ability to map a well's production history in Val Nav to a
  different UWI in Enersight's history DB. Use the new special mapping
  item "ProductionHistoryUWI".
- Fixed an issue in the export to Enersight where exporting rollups from
  VN 2020 and newer could result in extraneous production sets being
  created.
- Fixed an issue in the export to Enersight where an incorrect C\* value
  would sometimes be exported.
- Added the ability to export time-exponential ratio equations (in VN, n
  = 0) to Enersight, as semi-log ratios.
- Fixed an issue in the export to Enersight where the crown and freehold
  percentages in Enersight would be incorrect if a pooling factor was
  used to model the split in Val Nav.
- Fixed an issue in the export to Enersight where the resulting NRI
  would be incorrect when the Val Nav well had both a lease and
  overriding royalty (or lease revenue interest and net revenue
  interest).
- Added the ability to export time-linear ratio equations (in VN, n =
  -1) to Enersight.
- Fixed an issue in the import from Enersight, where sparse opex on
  different dates would not be imported correctly (the absence of a cost
  value on a given date would zero it, instead of allowing it to
  continue sparsely).
- Fixed an issue with the import from Enersight where the imported
  operating costs could start on the wrong date.
- Forecast exports to Enersight are now setting the 'Decline Keep
  Existing Rate Factor' flag so any RAF set in Enersight will be
  preserved. This will only impact Enersight 2.15 and newer.
- Fixed an issue in the import from Enersight where capital costs would
  sometimes not be imported.
- Added additional verbose logging to add additional clarity for
  forecasts that could not be exported.
