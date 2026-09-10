

# Install and Configure the Val Nav Integration Service

To install the Val Nav Integration Service:

1.  Obtain the installer for the Val Nav Integration Service from
    support, matching the version of Val Nav used with the target
    database.
2.  Install the service where deemed fit for its intended purpose
    1.  For those configuring the Val Nav-Execute integration, it is
        typically best, though not required, to install the Val Nav
        integration service on the same server that is hosting Execute.
        This greatly simplifies configuration.
3.  Edit the configuration of the Val Nav Integration Service
    (Eni.ValueNavigator.IntegrationService.exe.config) to provide:
    1.  Path to the Val Nav Project File (.vndl)
    2.  License key
    3.  ServiceUrl = http://localhost:8081
4.  Ensure the service account running the service has access rights to
    the VN database, if SQL or Oracle (e.g., an associated login in SQL
    Server or Oracle).
    1.  For Val Nav-Execute integrations, ensure this is the same domain
        service account that Execute’s service is configured with too.
    2.  If your Val Nav database is hosted in Oracle, you’ll need an
        appropriate version of the Oracle Client installed on the same
        machine as the Val Nav Integration Service.
5.  Restart the Val Nav Integration Service after making the above
    configuration changes.
6.  Ensure that the service account exists in Val Nav and is configured
    with appropriate permissions.



1.  



If your Val Nav database is hosted in Oracle, you’ll need an appropriate
version of the Oracle Client installed on the same machine as the Val
Nav Integration Service.



## Verify Installation of the Val Nav Integration Service

Once configured, the Val Nav Integration Service can be tested by
visiting `http://localhost:8081/swagger/ui/index` from a web-browser on
the machine running the Val Nav Integration Service. This will display
the API documentation.



![](../Images/Install-and-Configure-the-Val-Nav-Integration-Service-2.png)



Using the *swagger* interface, run `/api/system` and verify it returns
successfully. The version numbers returned in the Response Body will
help helpful to aid in any future troubleshooting.



![](../Images/Install-and-Configure-the-Val-Nav-Integration-Service-3.png)



The above should return a Response Body like the following. A failure
here would most likely indicate issues connecting to the underlying Val
Nav database, or a mismatch between the Val Nav Integration Service, and
Val Nav.

```

    {
       "DatabaseFilePath": "C:\\files\\vn_execute_integration_sql.vndl",
       "ServiceUserName": "SVC_AFENAV",
       "ValNavVersion": "21.2.0.3",
       "ValNavSchemaVersion": "2021.2.0.2",
       "IntegrationServiceVersion": "21.2.0.34",
       "ConnectionState": "Connected",
       "ServiceLogFilePath": "C:\\...\\Value Navigator Integration Service.log"
```

```
   }
        
```

Next, run `/api/currency` and verify it returns successfully.



![](../Images/Install-and-Configure-the-Val-Nav-Integration-Service-4.png)



It should return a currency like the following:

"\$US"

If the above two tests succeed, the Val Nav Integration Service is
probably configured correctly.
