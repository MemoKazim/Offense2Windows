>Misconfigured Group Policy Objects (GPOs) might lead Excessive access of some Units which cause Privilege escalation within domain
## Get-GPO

**Example Usage:**

``` Powershell
Get-GPO -All
```


**Advantages:**

·         Lists all GPOs in the domain.
·         Can be combined with Get-GPLink to find linked OUs.

**Possible Output:**

``` Output
DisplayName      : Default Domain Policy
DomainName       : acc.lab
Owner            : acc\Domain Admins
Id               : 31b2f340-016d-11d2-945f-00c04fb984f9
GpoStatus        : AllSettingsEnabled
Description      :
CreationTime     : 11/20/2023 7:04:49 PM
ModificationTime : 11/20/2023 7:54:08 PM
UserVersion      : AD Version: 0, SysVol Version: 0
ComputerVersion  : AD Version: 4, SysVol Version: 4
WmiFilter        :
```