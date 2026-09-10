



# Hardware and Software Requirements

## Architecture Overview

Value Navigator is a thick client desktop application that directly and
heavily interacts with a database server. As such, data locality is
paramount for optimal performance. Val Nav can be self-hosted in public
clouds (Azure SQL, AWS, etc.) or Citrix-style deployments, as many of
our customers do today.

## Scope of Support Regarding Self-Hosting

Our support team is here to assist you in successfully self-hosting Val
Nav. As experts in Val Nav, our focus is on ensuring the software
functions as expected within your chosen environment by:

- Providing an overview of how the software operates and interacts with
  its environment.
- Highlighting key considerations when virtualizing that could impact
  functionality, such as network latency, file sharing and user profile
  persistence.
- Outlining expected behavior and assisting on tests to validate them.

However, please note that the team are not application delivery experts
and specific questions on cloud platform configurations, infrastructure
setup or deployment strategies remain outside the scope of our support.
We recommend consulting with your internal IT team or a trusted cloud
service provider for guidance on these questions.

## File Syncing

Val Nav \*.vndb files (SQLite) should not be located on OneDrive,
DropBox, SharePoint or any kind of file syncing location. Their
proprietary syncing algorithms can occasionally introduce issues with
the SQLite database persistence mechanisms. This is especially true when
using those services for either multi-computer or multi-user sharing or
synchronization. We suggest you use manual copy-in/copy-out workflow so
the database is used on a non-synced location.

## Recommended Workstation

Quorum recommends the following minimum hardware and software
requirements for running
Value
Navigator.
Value
Navigator is compiled in 64-bit and will enable you to take
advantage of 64-bit operating systems.

| Hardware and Software | Requirements |
|----|----|
| CPU | Intel Core i3 or higher |
| Memory | 8 GB or higher |
| Video Resolution | 1280 x 1024 or higher. Recommend running at 100% DPI. |
| Operating System | Windows 7, 8, 10, or 11 |
| .NET Framework | 4.7.2 |
| Oracle Client | Oracle Client64-bit 10g, 11g, 12c, 18c, or 19c (where Val Nav is connecting to an Oracle database) |
| Network | \

Quorum recommends that this server be dedicated to
Value
Navigator and not shared with other applications.



## Supported Databases

Quorum requires the following minimum server requirements for running
Value
Navigator databases. Database maintenance is the responsibility
of the client, i.e. backup and restore policies. Azure SQL databases are
supported alongside Azure self-hosting deployments.

| Server | Requirements |
|----|----|
| Oracle | 64-bit 10g, 11g, 12c (version 12.1.0.2), 18c, or 19c |
| Microsoft SQL Server | 2008 R2, 2012, 2014, 2016, 2017, 2019, 2022, and 2025 |



SQLite, which is included with
Value
Navigator, creates file-based projects. SQLite projects do not
require a separate server component. SQLite databases are intended for
single-user access. They are not intended to be accessed over a network.



## Recommended Citrix Deployment

Value
Navigator and associated databases will function when deployed on
Citrix, but errors associated with these installations will not be
addressed by our Client Care team.

Quorum recommends the following deployment of
Value
Navigator on a Citrix Server:

- Save user profiles to a remote repository on log off of Citrix Server
- Restore user profiles from remote repository on log on of Citrix
  Server
- Store Product Key in the Eni.ValueNavigator.exe.config file
- Ensure that the %LOCALAPPDATA% and %APPDATA% exists on log on locally
  on the Citrix C drive
- Ensure that the Citrix server can access external files
- Ensure that the Citrix server can print to the network printers

## Application Server Provisioning (Citrix, Microsoft RDS, Terminal Server)

Recommended for use when: User workstations are \&gt;1ms from the Val Nav
database

- CPU cores: 4 minimum + 1 per concurrent user
- Memory: 8GB minimum + 2GB per concurrent user
- Operating system: Windows Server 2012 R2 minimum
- Software: .NET Framework 4.7.2
- Oracle Client64-bit 10g, 11g, 12c, 18c, or 19c (where Val Nav is
  connecting to an Oracle database)
- Network: \
