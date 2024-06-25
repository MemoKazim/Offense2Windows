>Sometimes administrators type sensitive information in PowerShell and forgot to delete them

### Get-PSReadLineOption

**Example Usage:**

``` Powershell
Get-PSReadLineOption | select HistorySavePath
```

This file contains all PowerShell commands which run in the system from initial setup

**Output:**

``` Output
HistorySavePath
---------------
C:\Users\USER\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\ConsoleHost_history.txt
```

