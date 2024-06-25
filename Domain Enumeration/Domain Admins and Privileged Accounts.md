>By enumerating privileged accounts you can find users which have excessive privilege and mark them as your target. 
## Get-ADGroupMember

**Example Usage:**

``` Powershell
Get-ADGroupMember -Identity "Domain Admins" | Select-Object Name, SamAccountName
```


**Advantages:**

·         Lists all members of the "Domain Admins" group.
·         Provides detailed information about each member.
·         Can filter and format output as needed.


**Possible Output:**

``` Output
distinguishedName : CN=Administrator,CN=Users,DC=acc,DC=lab
name              : Administrator
objectClass       : user
objectGUID        : a45c476a-77c6-4417-99e8-94d097fe6ae7
SamAccountName    : Administrator
SID               : S-1-5-21-1485720640-942268468-2087739954-500
```
