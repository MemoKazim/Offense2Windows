> Find user accounts that are safeguarded by AdminSDHolder.
### Script

**Example Usage:**

``` cmd
Import-Module ActiveDirectory
$protectedAccounts = Get-ADObject -Filter { adminCount -eq 1 } -Properties adminCount
$protectedAccounts | Select-Object Name, DistinguishedName
```

**Output:**

``` Output
Name                         DistinguishedName
----                         -----------------
Administrator                CN=Administrator,OU=BOSS Marcos,OU=EvilCorp,DC=namigsadigov,DC=ms2
Administrators               CN=Administrators,CN=Builtin,DC=namigsadigov,DC=ms2
Print Operators              CN=Print Operators,CN=Builtin,DC=namigsadigov,DC=ms2
Backup Operators             CN=Backup Operators,CN=Builtin,DC=namigsadigov,DC=ms2
Replicator                   CN=Replicator,CN=Builtin,DC=namigsadigov,DC=ms2
krbtgt                       CN=krbtgt,CN=Users,DC=namigsadigov,DC=ms2
Domain Controllers           CN=Domain Controllers,CN=Users,DC=namigsadigov,DC=ms2
Schema Admins                CN=Schema Admins,CN=Users,DC=namigsadigov,DC=ms2
Enterprise Admins            CN=Enterprise Admins,CN=Users,DC=namigsadigov,DC=ms2
Domain Admins                CN=Domain Admins,CN=Users,DC=namigsadigov,DC=ms2
Server Operators             CN=Server Operators,CN=Builtin,DC=namigsadigov,DC=ms2
Account Operators            CN=Account Operators,CN=Builtin,DC=namigsadigov,DC=ms2
Read-only Domain Controllers CN=Read-only Domain Controllers,CN=Users,DC=namigsadigov,DC=ms2
Key Admins                   CN=Key Admins,CN=Users,DC=namigsadigov,DC=ms2
Enterprise Key Admins        CN=Enterprise Key Admins,CN=Users,DC=namigsadigov,DC=ms2
Marcos MF. Feliciano         CN=Marcos MF. Feliciano,OU=BOSS Marcos,OU=EvilCorp,DC=namigsadigov,DC=ms2
```