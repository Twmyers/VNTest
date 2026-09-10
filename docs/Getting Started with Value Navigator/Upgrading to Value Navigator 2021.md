



# Upgrade Value Navigator Projects

Do not upgrade projects to by exporting an XML file from the original
version and importing it into a higher version. To ensure data is
upgraded successfully, follow the instructions below.

## Upgrade to 64 bit Version of Value Navigator

If you upgrade to the 64-bit version of
Value
Navigator and are using a ..udl or a ..vnudl to connect to a data
provider (e.g. a PPDM hub, or a database with capital actuals), you will
need to change the name of the provider from MSDORA.1 to
Devart.Data.Oracle. Open the .udl/.vnudl file in a text editor, such as
Notepad, and replace the “Provider” in the file.

We also recommended this with Windows versions 8 and up.

## Upgrade a Version 6.x or higher SQLite Project

Upgrade your project by opening the original version in the
Value
Navigator version you are upgrading to. An automatic upgrade will
begin. When you upgrade a SQLite project, a backup of the original
project is automatically created and saved in the same folder as the
original.

## Upgrade SQL Server or Oracle Projects (version 6 or higher)

Value
Navigator Oracle or SQL Server projects upgrade “in place” to the
current version of
Value
Navigator, meaning that once they have been upgraded, they can no
longer be run in the original version. We recommend you make a backup of
Oracle or SQL Server databases before upgrading them if you still want
to run them in the original version.

## Upgrade a Version 5.2 or older Project

If you are upgrading any
Value
Navigator 5.2 project, please contact
[Value Navigator Support](../../Support.md).

## Migrate Project Data to a Different Database Platform

To migrate to a different database platform, first upgrade your project
as described above, then export the XML from the upgraded project and
import it into a new project in the new platform.

 
