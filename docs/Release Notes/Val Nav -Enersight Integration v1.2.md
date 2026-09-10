

# Value Navigator- Enersight Integration v1.2

- Fixed issues with oil density in the export to
  Enersight
  where a default density would be used instead of the density entered
  on the well.
- Fixed an issue where Value Navigator and
  Enersight
  interpret segment end dates differently (VN as beginning of day, ES as
  end of day), which could result in small volume differences over time.
- Fixed an issue with forecasts that would fail to export to
  Enersightif
  there were a different number products in the different reserves
  categories.
- Fixed an issue where the Asset Name field was not working correctly.
- Fixed an issue with oil density to rely on static units instead of
  being dependent on user setting units in
  Enersight.
  Only works against
  Enersight
  2.14.
- Fixed an issue in timings-only imports from
  Enersight
  that could fail if there was no capital.
- Fixed the type well exports to send type well manual overrides if
  those exist. Was previously sending the calculated type well history
  instead.
- Now populates additional British Columbia royalty fields (balance
  effective date, remaining balance) newly added in
  Enersight.
- Added the ability to send a 'combined history and forecast' array, to
  enable easier synchronization of royalty balances, payouts, etc.
- Enhanced the import of
  Enersight
  user data into
  Value
  Navigator, doing type conversions (e.g., numeric to text)
  whenever needed.
- Split gas composition and gas energy content as separately mappable
  pieces of data.
- Added the ability to send wells to
  Enersight
  as templates. This will not set any fixed start dates and will set the
  'exclude from calculations' flag automatically.
- Updated the export of interests such that it only sends the interests
  for enabled companies to
  Enersight.
- Adds additional support for custom reserves category mappings, in both
  the export to and import from
  Enersight,
  for Value
  Navigator 2020.
- Added new options for the form of production arrays going to
  Enersight:
  can send as volume/date, rate/interval, rate/cumulative, including
  both CD and PD rate choices. Did not change the treatment of
  on-time/downtime in this situations at this time: all arrays are still
  sent over without downtime.
- Added error messaging to encourage the use of verbose logging, to aid
  in diagnosis and support.
- Added production history data to the verbose log.
