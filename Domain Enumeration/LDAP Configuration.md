> Review the LDAP configuration and access rights.
### Script

**Example Usage:**

``` Powershell
Import-Module ActiveDirectory; $domain = Get-ADDomain; $rootDSE = Get-ADRootDSE; Write-Output "LDAP Settings:`n--------------"; Write-Output "Domain Name: $($domain.Name)"; Write-Output "Domain Mode: $($domain.DomainMode)"; Write-Output "Forest Name: $($domain.Forest)"; Write-Output "LDAP Service Name: $($rootDSE.DnsHostName)"; Write-Output "LDAP Schema Naming Context: $($rootDSE.SchemaNamingContext)"; Write-Output "LDAP Configuration Naming Context: $($rootDSE.ConfigurationNamingContext)"; Write-Output "LDAP Default Naming Context: $($rootDSE.DefaultNamingContext)"
```

**Output:**

``` Output
LDAP Settings:
--------------
Domain Name: acc
Domain Mode: Windows2016Domain
Forest Name: acc.lab
LDAP Service Name: dc.acc.lab
LDAP Schema Naming Context: CN=Schema,CN=Configuration,DC=acc,DC=lab
LDAP Configuration Naming Context: CN=Configuration,DC=acc,DC=lab
LDAP Default Naming Context: DC=acc,DC=lab
```

**Example Usage:**

```Powershell
$ldapConfig = Get-ADRootDSE

$ldapConfig.configurationNamingContext

$ldapConfig.schemaNamingContext

$ldapConfig.defaultNamingContext

$ldapConfig.rootDomainNamingContext

$ldapConfig.dnsHostName
```

**Output:** 

```Output
CN=Configuration,DC=acc,DC=lab
CN=Schema,CN=Configuration,DC=acc,DC=lab
DC=acc,DC=lab
DC=acc,DC=lab
dc.acc.lab
```
