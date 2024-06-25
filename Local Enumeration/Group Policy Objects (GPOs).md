>Group Policies are important to define which computer has specified permission to given resource. Misconfigured policies might cause data breach, even privilege escalation!

### Get-GPO

**Example Usage:**

``` Powershell
Get-GPO -All
```


**Output**

``` Output
DisplayName      : Default Domain Policy
DomainName       : acc.lab
Owner            : acc\Domain Admins
Id               : 31b2f340-016d-11d2-945f-00c04fb984f9
GpoStatus        : AllSettingsEnabled
Description      :
CreationTime     : 11/20/2023 7:04:49 PM
ModificationTime : 11/20/2023 7:54:08 PM
UserVersion      : AD Version: 0, SysVol Version: 0
ComputerVersion  : AD Version: 4, SysVol Version: 4
WmiFilter        :

DisplayName      : Remote Desktop
DomainName       : acc.lab
Owner            : acc\Domain Admins
Id               : 33dffe37-1d11-466a-9f36-38e3dc0b9ae8
GpoStatus        : AllSettingsEnabled
Description      :
CreationTime     : 2/27/2024 3:40:22 PM
ModificationTime : 2/27/2024 4:24:20 PM
UserVersion      : AD Version: 0, SysVol Version: 0
ComputerVersion  : AD Version: 9, SysVol Version: 9
WmiFilter        :

DisplayName      : Default Domain Controllers Policy
DomainName       : acc.lab
Owner            : acc\Domain Admins
Id               : 6ac1786c-016f-11d2-945f-00c04fb984f9
GpoStatus        : AllSettingsEnabled
Description      :
CreationTime     : 11/20/2023 7:04:49 PM
ModificationTime : 11/20/2023 7:04:48 PM
UserVersion      : AD Version: 0, SysVol Version: 0
ComputerVersion  : AD Version: 1, SysVol Version: 1
WmiFilter        :
```


### gpupdate

**Example Usage:**

``` cmd
gpresult /R
```


**Output:**

``` Output
RSOP data for acc\Administrator on DC : Logging Mode
-----------------------------------------------------

OS Configuration:            Primary Domain Controller
OS Version:                  10.0.17763
Site Name:                   Default-First-Site-Name
Roaming Profile:             N/A
Local Profile:               C:\Users\Administrator
Connected over a slow link?: No


COMPUTER SETTINGS
------------------
    CN=DC,OU=Domain Controllers,DC=acc,DC=lab
    Last time Group Policy was applied: 5/30/2024 at 8:25:21 AM
    Group Policy was applied from:      dc.acc.lab
    Group Policy slow link threshold:   500 kbps
    Domain Name:                        acc
    Domain Type:                        Windows 2008 or later

    Applied Group Policy Objects
    -----------------------------
        Default Domain Controllers Policy
        Default Domain Policy
        Remote Desktop
        Local Group Policy

    The computer is a part of the following security groups
    -------------------------------------------------------
        BUILTIN\Administrators
        Everyone
        BUILTIN\Pre-Windows 2000 Compatible Access
        BUILTIN\Users
        Windows Authorization Access Group
        NT AUTHORITY\NETWORK
        NT AUTHORITY\Authenticated Users
        This Organization
        DC$
        Domain Controllers
        NT AUTHORITY\ENTERPRISE DOMAIN CONTROLLERS
        Authentication authority asserted identity
        Denied RODC Password Replication Group
        System Mandatory Level


USER SETTINGS
--------------
    CN=Administrator,CN=Users,DC=acc,DC=lab
    Last time Group Policy was applied: 5/30/2024 at 8:16:36 AM
    Group Policy was applied from:      dc.acc.lab
    Group Policy slow link threshold:   500 kbps
    Domain Name:                        acc
    Domain Type:                        Windows 2008 or later

    Applied Group Policy Objects
    -----------------------------
        N/A

    The following GPOs were not applied because they were filtered out
    -------------------------------------------------------------------
        Local Group Policy
            Filtering:  Not Applied (Empty)

    The user is a part of the following security groups
    ---------------------------------------------------
        Domain Users
        Everyone
        BUILTIN\Administrators
        BUILTIN\Users
        BUILTIN\Pre-Windows 2000 Compatible Access
        NT AUTHORITY\INTERACTIVE
        CONSOLE LOGON
        NT AUTHORITY\Authenticated Users
        This Organization
        LOCAL
        Group Policy Creator Owners
        Domain Admins
        Schema Admins
        Enterprise Admins
        Authentication authority asserted identity
        Denied RODC Password Replication Group
        High Mandatory Level
```


**Example Usage:**

**REQUIRES PRIVILEGE**

``` cmd
gpresult /r /scope:computer
```


``` Output
Microsoft (R) Windows (R) Operating System Group Policy Result tool v2.0
© 2018 Microsoft Corporation. All rights reserved.

Created on ‎5/‎30/‎2024 at 8:49:50 AM


RSOP data for  on DC : Logging Mode
------------------------------------

OS Configuration:            Primary Domain Controller
OS Version:                  10.0.17763
Site Name:                   Default-First-Site-Name
Roaming Profile:
Local Profile:
Connected over a slow link?: No


COMPUTER SETTINGS
------------------
    CN=DC,OU=Domain Controllers,DC=acc,DC=lab
    Last time Group Policy was applied: 5/30/2024 at 8:45:22 AM
    Group Policy was applied from:      dc.acc.lab
    Group Policy slow link threshold:   500 kbps
    Domain Name:                        acc
    Domain Type:                        Windows 2008 or later

    Applied Group Policy Objects
    -----------------------------
        Default Domain Controllers Policy
        Default Domain Policy
        Remote Desktop
        Local Group Policy

    The computer is a part of the following security groups
    -------------------------------------------------------
        BUILTIN\Administrators
        Everyone
        BUILTIN\Pre-Windows 2000 Compatible Access
        BUILTIN\Users
        Windows Authorization Access Group
        NT AUTHORITY\NETWORK
        NT AUTHORITY\Authenticated Users
        This Organization
        DC$
        Domain Controllers
        NT AUTHORITY\ENTERPRISE DOMAIN CONTROLLERS
        Authentication authority asserted identity
        Denied RODC Password Replication Group
        System Mandatory Level
```