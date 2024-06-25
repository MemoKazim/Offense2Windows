> Look for user accounts that have SID history attributes assigned.
### Powershell

**Example Usage:**

``` Powershell
Get-ADUser -Filter {SIDHistory -like '*'} -Property SIDHistory
```

**Output:**

``` Output
DistinguishedName : CN=John Doe,OU=Users,DC=example,DC=com
Enabled           : True
GivenName         : John
Name              : John Doe
ObjectClass       : user
ObjectGUID        : 11111111-2222-3333-4444-555555555555
SamAccountName    : johndoe
SIDHistory        : {S-1-5-21-1234567890-123456789-1234567890-1234, S-1-5-21-0987654321-987654321-9876543210-5678}
Surname           : Doe
UserPrincipalName : johndoe@example.com

DistinguishedName : CN=Jane Smith,OU=Users,DC=example,DC=com
Enabled           : True
GivenName         : Jane
Name              : Jane Smith
ObjectClass       : user
ObjectGUID        : 66666666-7777-8888-9999-000000000000
SamAccountName    : janesmith
SIDHistory        : {S-1-5-21-1234567890-123456789-1234567890-5678}
Surname           : Smith
UserPrincipalName : janesmith@example.com
```

### CMD

**Example Usage:**

``` cmd
dsquery * -filter "(sidHistory=*)" -attr distinguishedName
```

**Output:**

``` Output
CN=John Doe,OU=Users,DC=example,DC=com
CN=Jane Smith,OU=Users,DC=example,DC=com
CN=Finance Group,OU=Groups,DC=example,DC=com
CN=Server1,OU=Computers,DC=example,DC=com
CN=OldServiceAccount,OU=Service Accounts,DC=example,DC=com
```
