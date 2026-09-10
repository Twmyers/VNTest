

# Automate Spreadsheet Imports

You can create a batch file to import spreadsheet data automatically
using the command line below.

Command line:

Eni.ValueNavigator.exe /spreadsheet \ /file
\ /data \ /updatemode \ /authenticate /user
\ /password \ /logfile \ /checkversion
on\|off /month \ /proxy \ /ssimportlog \ /decline
\ /header \ /sheet \

See the arguments descriptions below.

| Arguments | Description |
| --- | --- |
| /file &lt;filepath&gt; | The path to the Value Navigator .vndl or .vndb file to open. (Required for Spreadsheet import) |
| /spreadsheet &lt;spreadsheet&gt; | The path to the spreadsheet template to import. (Required for Spreadsheet import) |
| /data &lt;area&gt; | The data area template to import with. Currently accepts the following as parameters: (Required for Spreadsheet import) Well Info and Custom Fields Reserves Category Custom Fields Project Start General Economics Declines Forecast Constants Incremental Parameters Plant Gas Properties - General Plant Gas Properties - Monthly Interests Manual Royalties Alberta Royalties B.C. Royalties Manitoba Royalties Newfoundland Royalties Nova Scotia Royalties Sask. Royalties New Brunswick Royalties Ontario Royalties Prince Edward Island Royalties Quebec Royalties Frontier Royalties United States Single Value Inputs United States Series Inputs Canada Single Value Inputs Canada Series Inputs Prices – Monthly Capital Costs Operating Costs Production History - Daily Production History - Daily to Monthly Production History - Annual to Monthly Production History Production Forecasts Opening Balances |
| /updatemode &lt;mode&gt; | The update mode for the spreadsheet import. (Required for Spreadsheet import) Merge Replace ReplaceAll |
| /authenticate | Indicates that the user will log in to the Value Navigator project using their Active Directory profile. Mutually exclusive with /name and /password and one or the other is required. |
| /user &lt;username&gt; | The name of the Value Navigator user that will log in to the project. Mutually exclusive with /authenticate and one or the other is required. |
| /password &lt;password&gt; | The password of the Value Navigator user that will log in to the project. This field is case-sensitive. Mutually exclusive with /authenticate and one or the other is required. |
| /logfile &lt;logpath&gt; | The path to the .log file where Value Navigator will record the results of its operations. If the file already exists, Value Navigator will append its messages to the end of the file. (Optional) |
| /checkversion on\|off | Determines whether Value Navigator should still proceed if the application version stored in the target project is different. The schema version must still match for the import to proceed. Default is On. (Optional) |
| /month &lt;month&gt; | Custom Current Month for spreadsheet import. Accepts months January to December as parameters. (Optional. Can only be used for the Data Area templates: Production History - Daily to Monthly Production History - Annual to Monthly Production History |
| /proxy &lt;proxy&gt; | The UWI proxy to use. (Optional.) Currently accepts the following as parameters: &lt;No Proxy&gt; Proxy - Vendor ID Proxy - API Number Proxy - Field Proxy - Field Code Proxy - Pool Proxy - Pool Code Proxy - Import Tag |
| /ssimportlog &lt;path&gt; | Outputs spreadsheet import messages to a file at the specified path. (Optional) |
| /decline &lt;slope&gt; | The decline display setting for nominal/tangent/secant declines on import. (Required for Declines Data Area template and can only be used with that template) Accepts the following as parameters: Nominal Effective Tangent Effective Secant |
| /header &lt;offset&gt; | The number of header rows that can be used to determine the data starting point. Default is 2. (Optional) |
| /sheet &lt;name&gt; | The name of the sheet to import. (Optional) |
