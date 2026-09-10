

# Integrate Val Nav with Reserves

The Val Nav Integration Service provides a way for other applications to
interact with a Val Nav database. It runs as a Windows service which
will start automatically when Windows starts up. Other applications (for
example, petroLook) can access the service by calling the web service
and getting results back in JSON format.

## Installation

Follow the instructions for manual installation if the server already
has another service named ValNavIntegrationService, otherwise the
installation will overwrite the existing service with the same name.

### Install ValNav Integration Service Using the Wizard

 

1.  Download latest version of ValNav Integration Service from
    \\cgysvrfile03\Common\TFSBuilds\ValueNavigator\Tools\Val Nav
    Service\\ .
    
2.  Run the ValNavIntegrationService.x64
    installation wizard.
    
3.  Click Next when prompted to continue
    installation.
    
4.  Accept the License Agreement, and click
    Next.
    
5.  Define the Destination Folder for the ValNav Integration Service
    install (below is the default destination), and click
    Next.
    
6.  Click Install .
    
7.  Click Yes when asked to allow
    ValNavIntegrationService to make changes to your device.
    
8.  Click Finish when installation is
    completed .

## Configure ValNav Integration Service

 

1.  Create a project with SQL database (with corresponding .vndl file).
    
2.  Create a ValNav user (using Import from AD) with the same name as
    the Service account used for ValNav Integration Services and grant
    the user the Super Users role. See [Create Users](../Administration/Configure%20User%20Security/Create%20Users.md) for more information.
    

### Configure Log-On-As account

 

1.  Open Services, navigate to Value Navigator
    Integration Service 2020, and right-click to select
    Properties.
    
2.  On the  Log On tab, click
    This account, and enter the
    following:
    1.  This account = service account for Quorum Reserves that is also
        a user in ValNav
    2.  Password/Confirm password = password for service account entered
3.  Click OK.
4.  Restart the Value Navigator Integration Service 2020 for the new
    Log-On-As account to take effect.

### Update applicationSettings in Eni.ValueNavigator.IntegrationService.exe.config file

 

1.  Navigate to the Destination Folder where the ValNav Integration
    Service was installed (default is C:\Program Files\Quorum
    Software\Value Navigator Integration Service 2020).
2.  Open the Eni.ValueNavigator.IntegrationService.exe.config file with
    Notepad.
3.  Scroll down to the applicationSettings section (lines 132 to 153 of
    the file).
    
4.  Edit the following:
    1.  Path to the .VNDL file
    2.  (Optional) Port number (only if default 8081 is already
        used/registered by another process)
    3.  ValNav license key
5.  Save the changes.
6.  Restart the Value Navigator Integration Service 2020 for the new
    applicationSettings to take effect.

## Configure Quorum Reserves

### Configure Security

Set the security privileges for the appropriate role(s) to
Grant for the Object Type
ValNav Configuration.



### Configure Metadata

 

1.  Create metadata groups for context(s) to import. For testing, each
    type of VN variable is its own group.
    
2.  Create metadata columns for each group.
    
    
3.  Add new metadata groups to context(s) to import.
    

 

### Configure the SQL Database

 

Create a database table for each metadata group.





### Configure Reserves/Val Nav Integration

 

#### Create a New Configuration

 

1.  Go to Integration \&gt;
    Configuration \&gt;
    Val Nav.
    
2.  Select the appropriate Context for the Val Nav loader, then click
    Create.
    
3.  Enter the Configuration Name.
    
4.  Enter the URL of the ValNav Integration Service (as entered in the
    Eni.ValueNavigator.IntegrationService.exe.config file), and then
    click Refresh .
    
5.  After the URL is refreshed, click
    Save.
    

#### Add Metadata Groups

 

1.  In Settings, select the ValNav
    variable groups, reserve categories, and products.
    
2.  For each Metadata Group, map AR metadata to VN variables. )

#### Loader Definition and Option

 

1.  Create a Loader Definition (VNLoader) and adda Loader Option
    (ValNavOptionControl).
    
2.  Select a ValNav Configuration to use in the
    Loader Options definition.
    

## Load ValNav Data

 

1.  Once the installation, setup, and configurations are complete, go to
    Data \&gt; Data
    Versions \&gt; Load Data, and the
    ValNav Loader.
    
    

    Selecting a Hierarchy changes how the ValNav entities are displayed
    in the hierarchy tree.

    
2.  Select a Plan (Working, Accepted, etc.) and Scenario that have the
    required ValNav data for import.
3.  Click Load to begin the load.

Once the load is successfully completed, data is populated in the
PLS_VN_ECON_OBJECT table, as well as Attribute and Econ stage tables
mapped in the ValNav Integration configuration



## Mapping Rules

### General

- Any variables that are mapped (has the notepad/pencil button in Edit)
  but blank will cause an error. This can happen if you open the edit
  window for a variable but click OK without mapping anything.
- Mapping ValNav products that were not selected in the Settings will
  cause an error.

### Attributes

- LINK_ID metadata must be Version Descriptor
- OBJECT_ID metadata must be ObjectIdentifier Descriptor
- OBJECT_NAME metadata must be ObjectName Descriptor
- OBJECT_NAME, ENTITY_ID, and RESERVE_CATEGORY_ID cannot be mapped with
  anything
- ValNav ENTITY_ID cannot be used to map anything

### Econ

- Must include LINK_ID, OBJECT_ID, PERIOD, and PERIOD_TYPE metadata

## Other Notes

These settings set the request batch size
(ValNavToEconLoader.CaseRequestLimit) and whether the job log shows
debug information (ValNavToEconLoader.DebugMode). CaseRequestLimit value
should not be greater than 200.



The toggle shown below controls if the PLS_VN_ECON_OBJECT table is
cleared (true) or not cleared (false) after a load.



## Configuration

The configuration for the service is stored in the install directory
(typically C:\Program Files\Quorum\Value Navigator Integration Service
2020\\, in the file Eni.ValueNavigator.IntegrationService.exe.config.
You can edit this file in a text editor. This file includes two sets of
settings:

- \ contains normal Val Nav configuration (documented
  elsewhere)
- \ controls the service, per the following:

| Setting | Description |   |
|----|----|----|
| ProjectFilePath | The path to the project file (.vndb) or the data link file (.vndl) containing the connection information for the Val Nav database. | C:\data\2018.vndl |
| ServiceUrl | Sets the port that the service runs on. | http://localhost:8081 |
| LicenseKey | Fill in your license key here, or leave blank to use an existing license that has already been configured through Val Nav. |  |
| LicensePollPeriod | The interval that the license server will wait before retrying when it can’t acquire a license (hh:mm:ss). | 00:01:00 |
| SessionTimeout | The length of time that the service will wait for a response from the database before aborting and disconnecting. Set to zero to disable the timeout and wait forever. (hh:mm:ss) | 00:05:00 |

After editing the configuration file, go to the Services control panel
and restart the integration service to apply the changes.

## Using the Web Service

Once the service is up and running you can check it by connecting to it
in your browser

## Authentication

The integration service has a multi-level authentication check. By
default, it is set up to pass through the Windows identity of the
calling application.

1.  Client identity calling the web service is checked.
2.  If using SQL Server with Windows Authentication, client identity is
    checked against SQL Server. Calling the web service is checked
    against SQL Server.
    1.  If integrating with Quorum Execute, the Execute service account
        must be added as a SQL Server user on the SQL Server database.
3.  Client identity checked against internal Val Nav security.
    1.  By default, uses Windows user name of calling identity.

    

    1.  User name can be overridden using custom header “ValNavUser”.
4.  Once a "ValNavUser" is derived, we determine if the user is valid
    by:
    1.  Checking normal Val Nav security for said user name.

    

    1.  For testing only: When the database is a default setup where one
        and only one user exists (the admin user), then any ValNavUser
        is authorized

## Troubleshooting

### Log file

The service logs requests to a log file that you can use to troubleshoot
any problems. This log file is stored in the following location for the
service-executing account (by default, the Local System account,
SYSTEM):

%LOCALAPPDATA%\Quorum\Value Navigator Integration Service 2020\Value
Navigator Integration Service.log.

On 64-bit versions of Windows, this is the following path for the Local
System user:

C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Quorum\Value
Navigator Integration Service 2020\Value Navigator Integration
Service.log.

By default, this path might not be visible/accessible in Windows
Explorer. You might have to navigate to each folder in turn and get
prompted to allow access to each folder. You can change the log file
path by editing the Eni.ValueNavigator.IntegrationService.exe.config
file. Change the fileName variable of the Rolling File Log under the
\ node, and restart the service.
