>By knowing Organizational Unit's hierarchy you can understand policy applications to specified Units
## Get-ADOrganizationalUnit

``` Powershell
Get-ADOrganizationalUnit -Filter * | Select-Object Name, DistinguishedName
```

**Advantages:**

·         Lists all OUs within the domain.
·         Provides the Distinguished Name (DN) for each OU, which shows the hierarchy.
·         Simple and straightforward to use.


**Possible Output:**

| Name         | DistinguishedName                               |
| ------------ | ----------------------------------------------- |
| HR           | OU=HR,DC=example,DC=com                         |
| IT           | OU=IT,DC=example,DC=com                         |
| Finance      | OU=Finance,DC=example,DC=com                    |
| Operations   | OU=Operations,DC=example,DC=com                 |
| NorthAmerica | OU=NorthAmerica,OU=Operations,DC=example,DC=com |
| Europe       | OU=Europe,OU=Operations,DC=example,DC=com       |
