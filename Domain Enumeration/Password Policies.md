>Weak passwords lead account compromises.

### Get-ADDefaultDomainPasswordPolicy

**Example Usage:**

``` Powershell
Get-ADDefaultDomainPasswordPolicy
```


**Output:**

``` Output
ComplexityEnabled           : False
DistinguishedName           : DC=acc,DC=lab
LockoutDuration             : 00:01:00
LockoutObservationWindow    : 00:01:00
LockoutThreshold            : 0
MaxPasswordAge              : 42.00:00:00
MinPasswordAge              : 1.00:00:00
MinPasswordLength           : 4
objectClass                 : {domainDNS}
objectGuid                  : eef5685e-7aea-41eb-b95b-0cb0192d956f
PasswordHistoryCount        : 24
ReversibleEncryptionEnabled : False
```


### net

**Example Usage:**

``` cmd
net accounts /domain
```

**Output:**

``` Output
Force user logoff how long after time expires?:       Never
Minimum password age (days):                          1
Maximum password age (days):                          42
Minimum password length:                              4
Length of password history maintained:                24
Lockout threshold:                                    Never
Lockout duration (minutes):                           1
Lockout observation window (minutes):                 1
Computer role:                                        PRIMARY
The command completed successfully.
```
