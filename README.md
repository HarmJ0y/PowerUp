#PowerUp

PowerUp is a powershell tool to assist with local privilege escalation on 
Windows systems. It contains several methods to identify and abuse
vulnerable services.

PowerUp was developed by [@harmj0y](https://twitter.com/harmj0y).


## Service Enumeration:
    Get-ServiceUnquoted             -   returns services with unquoted paths that also have a space in the name
    Get-ServiceEXEPerms             -   returns services where the current user can write to the service binary path
    Get-ServicePerms                -   returns services the current user can modify


## Service Abuse:
    Invoke-ServiceUserAdd           -   modifies a modifiable service to create a user and add it to the local administrators
    Write-UserAddServiceBinary      -   writes out a patched C# service binary that adds a local administrative user
    Write-ServiceEXE                -   replaces a service binary with one that adds a local administrator user
    Restore-ServiceEXE              -   restores a replaced service binary with the original executable


## Misc. Helpers:
    Invoke-ServiceStart             -   starts a given service
    Invoke-ServiceStop              -   stops a given service
    Invoke-ServiceEnable            -   enables a given service
    Invoke-ServiceDisable           -   disables a given service
    Get-ServiceDetails              -   returns detailed information about a service

