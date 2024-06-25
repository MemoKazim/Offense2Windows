>By checking system uptime you can determine if system has required security updates, such as hotfixes

### Get-CIMInstance

**Example Usage:**

``` Powershell
Get-CimInstance -ClassName Win32_OperatingSystem | Select-Object LastBootUpTime
```


**Output:**

``` Output
LastBootUpTime
--------------
5/23/2024 4:26:58 PM
```


### systeminfo

**Example Usage:**

``` cmd
systeminfo | find "System Boot Time"
```


**Output:**

``` Output
System Boot Time:          5/23/2024, 4:26:58 PM
```

