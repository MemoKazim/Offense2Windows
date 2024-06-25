> Examine the settings and configurations of Kerberos policies.
### Powershell

**Example Usage:**

``` Powershell
(Get-ADDefaultDomainPasswordPolicy | Select-Object MaxTicketAge, MaxRenewAge, MaxServiceAge, MaxClockSkew, TicketGrantingTicketRenewal) | Format-List
```

**Output:**

``` Output
MaxTicketAge                  : 10:00:00:00
MaxRenewAge                   : 7:00:00:00
MaxServiceAge                 : 1:00:00:00
MaxClockSkew                  : 0:00:00:05
TicketGrantingTicketRenewal   : 1:00:00:00
```