> Enumerate all computer accounts that are part of the domain.
### Powershell

**Example Usage:**

``` Powershell
Get-ADComputer -Filter * -Property *
```

**Output:**

``` Output
AccountExpirationDate                :
accountExpires                       : 9223372036854775807
AccountLockoutTime                   :
AccountNotDelegated                  : False
AllowReversiblePasswordEncryption    : False
AuthenticationPolicy                 : {}
AuthenticationPolicySilo             : {}
BadLogonCount                        : 0
badPasswordTime                      : 0
badPwdCount                          : 0
CannotChangePassword                 : False
CanonicalName                        : acc.lab/Domain Controllers/DC
Certificates                         : {}
CN                                   : DC
codePage                             : 0
CompoundIdentitySupported            : {False}
countryCode                          : 0
Created                              : 11/20/2023 7:06:18 PM
createTimeStamp                      : 11/20/2023 7:06:18 PM
Deleted                              :
Description                          :
DisplayName                          : DC$
DistinguishedName                    : CN=DC,OU=Domain Controllers,DC=acc,DC=lab
DNSHostName                          : dc.acc.lab
DoesNotRequirePreAuth                : False
dSCorePropagationData                : {2/19/2024 9:22:30 AM, 11/20/2023 7:06:18 PM, 1/1/1601 3:04:16 AM}
Enabled                              : True
HomedirRequired                      : False
HomePage                             :
instanceType                         : 4
IPv4Address                          : 192.168.30.121
IPv6Address                          :
isCriticalSystemObject               : True
isDeleted                            :
KerberosEncryptionType               : {RC4, AES128, AES256}
LastBadPasswordAttempt               :
LastKnownParent                      :
lastLogoff                           : 0
lastLogon                            : 133615194797872078
LastLogonDate                        : 5/20/2024 8:32:18 AM
lastLogonTimestamp                   : 133606567386308341
localPolicyFlags                     : 0
Location                             :
LockedOut                            : False
logonCount                           : 784
ManagedBy                            :
MemberOf                             : {}
MNSLogonAccount                      : False
Modified                             : 5/20/2024 8:32:18 AM
modifyTimeStamp                      : 5/20/2024 8:32:18 AM
msDFSR-ComputerReferenceBL           : {CN=WIN-H8S721374JH,CN=Topology,CN=Domain System Volume,CN=DFSR-GlobalSettings,CN=System,DC=acc,DC=lab}
msDS-AdditionalDnsHostName           : {WIN-H8S721374JH $, DC $}
msDS-GenerationId                    : {22, 168, 230, 55...}
msDS-SupportedEncryptionTypes        : 28
msDS-User-Account-Control-Computed   : 0
Name                                 : DC
nTSecurityDescriptor                 : System.DirectoryServices.ActiveDirectorySecurity
ObjectCategory                       : CN=Computer,CN=Schema,CN=Configuration,DC=acc,DC=lab
ObjectClass                          : computer
ObjectGUID                           : 78700988-48fb-49a7-9315-e1348833d4a4
objectSid                            : S-1-5-21-1485720640-942268468-2087739954-1000
OperatingSystem                      : Windows Server 2019 Datacenter
OperatingSystemHotfix                :
OperatingSystemServicePack           :
OperatingSystemVersion               : 10.0 (17763)
PasswordExpired                      : False
PasswordLastSet                      : 5/2/2024 5:08:05 AM
PasswordNeverExpires                 : False
PasswordNotRequired                  : False
PrimaryGroup                         : CN=Domain Controllers,CN=Users,DC=acc,DC=lab
primaryGroupID                       : 516
PrincipalsAllowedToDelegateToAccount : {}
ProtectedFromAccidentalDeletion      : False
pwdLastSet                           : 133590892857434163
rIDSetReferences                     : {CN=RID Set,CN=DC,OU=Domain Controllers,DC=acc,DC=lab}
SamAccountName                       : DC$
sAMAccountType                       : 805306369
sDRightsEffective                    : 15
serverReferenceBL                    : {CN=DC,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=acc,DC=lab}
ServiceAccount                       : {}
servicePrincipalName                 : {TERMSRV/DC, TERMSRV/dc.acc.lab, Dfsr-12F9A27C-BF97-4787-9364-D31B6C55EB04/dc.acc.lab, ldap/WIN-H8S721374JH/acc...}
ServicePrincipalNames                : {TERMSRV/DC, TERMSRV/dc.acc.lab, Dfsr-12F9A27C-BF97-4787-9364-D31B6C55EB04/dc.acc.lab, ldap/WIN-H8S721374JH/acc...}
SID                                  : S-1-5-21-1485720640-942268468-2087739954-1000
SIDHistory                           : {}
TrustedForDelegation                 : True
TrustedToAuthForDelegation           : False
UseDESKeyOnly                        : False
userAccountControl                   : 532480
userCertificate                      : {}
UserPrincipalName                    :
uSNChanged                           : 147497
uSNCreated                           : 12293
whenChanged                          : 5/20/2024 8:32:18 AM
whenCreated                          : 11/20/2023 7:06:18 PM
```

### CMD

**Example Usage:**

``` cmd
dsquery computer -limit 0
```

**Output:**

``` Output
"CN=DC,OU=Domain Controllers,DC=acc,DC=lab"
"CN=FILE,CN=Computers,DC=acc,DC=lab"
"CN=cl-01,OU=IT,DC=acc,DC=lab"
"CN=cl-02,CN=Computers,DC=acc,DC=lab"
"CN=cl-03,CN=Computers,DC=acc,DC=lab"
"CN=cl-04,CN=Computers,DC=acc,DC=lab"
"CN=cl-05,CN=Computers,DC=acc,DC=lab"
"CN=cl-06,CN=Computers,DC=acc,DC=lab"
"CN=cl-07,CN=Computers,DC=acc,DC=lab"
"CN=cl-08,CN=Computers,DC=acc,DC=lab"
"CN=cl-09,CN=Computers,DC=acc,DC=lab"
"CN=cl-10,CN=Computers,DC=acc,DC=lab"
"CN=cl-11,CN=Computers,DC=acc,DC=lab"
"CN=COMMANDO,CN=Computers,DC=acc,DC=lab"
```
