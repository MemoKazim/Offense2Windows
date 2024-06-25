>By knowing SPNs you can perform Kerberos attacks such as kerberoasting
## Get-ADServiceAccount

**Example usage:**

``` Powershell
Get-ADServiceAccount -Filter * -Properties PrincipalsAllowedToDelegateToAccount | Select-Object Name, PrincipalsAllowedToDelegateToAccount
```

``` Powershell
Get-ADUser -Filter {ServicePrincipalName -ne "$null"} -Property ServicePrincipalName
```

**Advantages:**

·         Lists SPNs for all user accounts in the domain.
·         Can filter and format the output as needed.


**Possible Output:**

``` Output
DistinguishedName        : CN=mssql_svc,CN=Users,DC=acc,DC=lab
Enabled                  : True
GivenName                :
Name                     : mssql_svc
ObjectClass              : user
ObjectGUID               : e84f7093-2c15-4c8f-bbe4-7c923eaa61a5
SamAccountName           : mssql_svc
ServicePrincipalName     : {mssql_svc/mssqlserver.change.me}
SID                      : S-1-5-21-1485720640-942268468-2087739954-1315
Surname                  :
UserPrincipalName        :
```


### Get-ADComputer

``` Powershell
Get-ADComputer -Filter {ServicePrincipalName -ne "$null"} -Property ServicePrincipalName
```

**Advantages:**

·         Lists SPNs for all computer accounts in the domain.
·         Can filter and format the output as needed.


**Possible Output:**

``` Output
DistinguishedName    : CN=DC,OU=Domain Controllers,DC=acc,DC=lab
DNSHostName           : dc.acc.lab
Enabled                       : True
Name                          : DC
ObjectClass                 : computer
ObjectGUID                 : 78700988-48fb-49a7-9315-e1348833d4a4
SamAccountName      : DC$
ServicePrincipalName : {TERMSRV/DC, TERMSRV/dc.acc.lab, Dfsr-12F9A27C-BF97-4787-9364-D31B6C55EB04/dc.acc.lab, ldap/WIN-H8S721374JH/acc...}
SID                              : S-1-5-21-1485720640-942268468-2087739954-1000
UserPrincipalName     :
```

