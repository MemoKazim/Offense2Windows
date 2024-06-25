>Enumerating domain users gives you opportunity to know which users have specified permission.
>Sometimes you can find overly privileged accounts which can be exploited
## Get-ADUser

``` Powershell
Get-ADUser -Filter * -Properties *
```

**Advantages:**

·         Lists all user accounts in the domain.
·         Provides detailed information about each user account.
·         Can filter and format output as needed.


**Example Usage:**

``` Powershell
Get-ADUser -Filter * -Property DisplayName, SamAccountName, Enabled, PasswordLastSet, LastLogonDate, MemberOf | Format-Table DisplayName, SamAccountName, Enabled, PasswordLastSet, LastLogonDate
```


**Possible Output:**

| DisplayName   | SamAccountName | Enabled | PasswordLastSet     | LastLogonDate       |
| ------------- | -------------- | ------- | ------------------- | ------------------- |
| John Doe      | jdoe           | True    | 2024-01-10 12:34:56 | 2024-05-20 10:20:30 |
| Jane Smith    | jsmith         | True    | 2023-12-05 08:15:22 | 2024-05-22 09:45:12 |
| Admin User    | admin          | True    | 2024-01-15 14:02:11 | 2024-05-23 11:30:45 |
| Disabled User | duser          | False   | 2022-05-10 16:25:30 | 2022-06-01 09:10:00 |


### dsquery

**Example Usage:**

``` cmd
dsquery user -limit 0
```

**Advantages:**

·         Simple and quick way to list all user accounts.
·         Outputs distinguished names of user accounts.


**Possible Output:**

``` Output
"CN=John Doe,CN=Users,DC=example,DC=com"
"CN=Jane Smith,CN=Users,DC=example,DC=com"
"CN=Admin User,CN=Users,DC=example,DC=com"
"CN=Disabled User,CN=Users,DC=example,DC=com"
```

### Get-ADUser

**Example Usage:**

``` Powershell
Get-ADUser -Filter * -Property DisplayName, SamAccountName, Enabled, PasswordLastSet, LastLogonDate, MemberOf | Where-Object { $_.Enabled -eq $true } | Format-Table DisplayName, SamAccountName, PasswordLastSet, LastLogonDate
```


**Possible Output:**

| DisplayName | SamAccountName | PasswordLastSet     | LastLogonDate       |
| ----------- | -------------- | ------------------- | ------------------- |
| John Doe    | jdoe           | 2024-01-10 12:34:56 | 2024-05-20 10:20:30 |
| Jane Smith  | jsmith         | 2023-12-05 08:15:22 | 2024-05-22 09:45:12 |
| Admin User  | admin          | 2024-01-15 14:02:11 | 2024-05-23 11:30:45 |

### Get-ADObject

**Example Usage**:

```Powershell
Get-ADObject -LDAPFilter "(objectClass=User)"
```

By typing special LDAP queries you can find Active Directory objects easily

**Possible Output**:

```Output

DistinguishedName                                         Name                 ObjectClass                ObjectGUID
-----------------                                         ----                 -----------                ----------
CN=Administrator,CN=Users,DC=acc,DC=lab                   Administrator        user                       a45c476a-77c6-4417-99e8-94d097fe6ae7
CN=Guest,CN=Users,DC=acc,DC=lab                           Guest                user                       4e2e598e-bfcb-488a-b54a-f42e2bea7277
CN=DC,OU=Domain Controllers,DC=acc,DC=lab                 DC                   computer                   78700988-48fb-49a7-9315-e1348833d4a4
CN=krbtgt,CN=Users,DC=acc,DC=lab                          krbtgt               user                       27cee02f-0730-43b5-972b-25ce8fff82ce
CN=Melba Analise,CN=Users,DC=acc,DC=lab                   Melba Analise        user                       270878cf-e7af-40fb-9d1e-92d25215453c
CN=Pat Joya,CN=Users,DC=acc,DC=lab                        Pat Joya             user                       0c803865-0d19-4501-8fce-92793e608407
```