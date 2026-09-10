

# Install Access Database Engine

ARIES databases are stored as Microsoft Access database files. To use
these databases with
Value
Navigator, you need the correct version of the Access Database
Engine. If you have 32-bit
Value
Navigator, you need the 32-bit engine, and if you have 64-bit
Value
Navigator, you need the 64-bit engine.



As of version 2018,
Value
Navigator no longer supports 32-bit installations.



If you are running 64-bit
Value
Navigator on a machine with 64-bit Office, installing the 64-bit
version of MS Access will not be a problem. However, if you try to
install 64-bit Access on a machine with 32-bit Office, you'll get the
following error:  "You cannot install the 64-bit version of Microsoft
Access Database Engine because you currently have 32-bit products
installed." To overcome this limitation, follow the procedure below.

## 64-bit Value Navigator with 32 bit Office or Access Database Engine

To install the Access Database Engine

1.  Use regedit to check for the registry setting for mso.dll:
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Common\FilesPaths\mso.dll
2.  If the key exists, the 64-bit engine is installed and you are done
3.  If the key does not exist, force install the 64-bit engine via the
    command line from the install files folder:
    AccessDatabaseEngine_x64.exe /passive
4.  Using regedit again, delete or rename the mso.dll entry above that
    was added as part of the 64-bit install. (This step is not necessary
    to use
    Value
    Navigator, but if not completed will cause all Office
    programs to show a ‘reconfiguring’ dialog at startup.)
