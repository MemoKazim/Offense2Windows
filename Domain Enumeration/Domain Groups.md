>Some misconfigured group and their members might have privileges which theoretically should not have which may lead privilege escalation
### Get-ADGroup

**Example Usage**:

```
Get-ADGroup -Filter * -Properties * | Select-Object Name, GroupCategory, GroupScope, Description, DistinguishedName
```


**Advantages:**

·         Retrieves all groups in


**Possible Output:**

```Output
Name              : Administrators
GroupCategory     : Security
GroupScope        : DomainLocal
Description       : Administrators have complete and unrestricted access to the computer/domain
DistinguishedName : CN=Administrators,CN=Builtin,DC=acc,DC=lab
```


### Remote Management Group

>This Group members have access to domain controller directly. Checking them might be useful

**Example Usage**

```Powershell
Get-ADGroupMember -Identity "Remote Management Users"
```

**Possible Output:**

```Output
distinguishedName : CN=Marcos Silva,OU=IT,DC=acc,DC=lab
name              : Marcos Silva
objectClass       : user
objectGUID        : 4a1537bc-76af-4780-9ab4-7ee9b04b3d25
SamAccountName    : msilva
SID               : S-1-5-21-1485720640-942268468-2087739954-2104
```