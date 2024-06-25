>By checking event log you can understand latest system activities

### Get-EventLog

**Example Usage:**

``` Powershell
Get-EventLog -List
```

``` Powershell
Get-EventLog -LogName Security -Newest 50 -EntryType < Error | FailureAudit | Information | SuccessAudit | Warning >
```

``` Powershell
Get-WinEvent -FilterHashtable @{LogName="Security"; Id=4624}
```


**Output:**

``` Output

  Max(K) Retain OverflowAction        Entries Log
  ------ ------ --------------        ------- ---
     512      7 OverwriteOlder            345 Active Directory Web Services
  20,480      0 OverwriteAsNeeded      34,807 Application
  15,168      0 OverwriteAsNeeded         332 DFS Replication
     512      0 OverwriteAsNeeded       1,062 Directory Service
 102,400      0 OverwriteAsNeeded         386 DNS Server
  20,480      0 OverwriteAsNeeded           0 HardwareEvents
     512      7 OverwriteOlder              0 Internet Explorer
  20,480      0 OverwriteAsNeeded           0 Key Management Service
     512      7 OverwriteOlder                Parameters
 131,072      0 OverwriteAsNeeded     192,494 Security
     512      7 OverwriteOlder                State
  20,480      0 OverwriteAsNeeded      58,686 System
  15,360      0 OverwriteAsNeeded         386 Windows PowerShell
```

``` Output

   Index Time          EntryType   Source                 InstanceID Message
   ----- ----          ---------   ------                 ---------- -------
  572590 May 29 09:47  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572589 May 29 09:47  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572588 May 29 09:47  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
  572587 May 29 09:46  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572586 May 29 09:46  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572585 May 29 09:46  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
  572584 May 29 09:45  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572583 May 29 09:45  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572582 May 29 09:45  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
  572581 May 29 09:44  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572580 May 29 09:44  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572579 May 29 09:44  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572578 May 29 09:44  SuccessA... Microsoft-Windows...         4634 An account was logged off....
  572577 May 29 09:44  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572576 May 29 09:44  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
  572575 May 29 09:44  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572574 May 29 09:44  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
  572573 May 29 09:44  SuccessA... Microsoft-Windows...         4624 An account was successfully logged on....
  572572 May 29 09:44  SuccessA... Microsoft-Windows...         4672 Special privileges assigned to new logon....
```


``` Output


   ProviderName: Microsoft-Windows-Security-Auditing

TimeCreated                     Id LevelDisplayName Message
-----------                     -- ---------------- -------
5/30/2024 8:51:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:50:22 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:50:22 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:50:22 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:50:22 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:50:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:49:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:48:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:47:49 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:47:23 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:47:23 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:47:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:46:21 AM          4624 Information      An account was successfully logged on....
5/30/2024 8:45:22 AM          4624 Information      An account was successfully logged on....
```

### Wevtutil

**Example Usage:**

``` cmd
Wevtutil el
```

``` cmd
Wevtutil gl Security
```

**Output**

``` Output
name: Security
enabled: true
type: Admin
owningPublisher:
isolation: Custom
channelAccess: O:BAG:SYD:(A;;0xf0005;;;SY)(A;;0x5;;;BA)(A;;0x1;;;S-1-5-32-573)
logging:
  logFileName: %SystemRoot%\System32\Winevt\Logs\Security.evtx
  retention: false
  autoBackup: false
  maxSize: 20971520
publishing:
  fileMax: 1
```
