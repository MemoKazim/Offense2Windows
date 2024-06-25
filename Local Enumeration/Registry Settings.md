## Interesting registry entries

>By checking significant registry settings you might be able to find potentially harmful and/or confidential data

### Environmental variables

```Powershell
reg query "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Environment"

reg query "HKCU\Environment"
```

### Network Interface

```Powershell
reg query "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces\"
```
This will show all available network interfaces. By appending ID of interface to reg query you can find more information

### Domain Information

```Powershell
reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Group Policy\History"
```

### Installed Software

```Powershell
reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Uninstall"
```

### Remote Terminal & Management

```Powershell
reg query "HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server"

reg query "HKLM\Software\Policies\Microsoft\Windows NT\Terminal Services"

reg query "HKCU\Software\Microsoft\Terminal Server Client\Servers"

reg query "HKCU\Software\Microsoft\Terminal Server Client\Default"
```

### Group Policy 

```Powershell
 eg query "HKLM\Software\Policies\Microsoft\Windows\System"
```

### Audit Settings

```Powershell
reg query "HKLM\SYSTEM\CurrentControlSet\Control\Lsa"
```

### Windows Defender State

```Powershell
reg query "HKLM\Software\Microsoft\Windows Defender"

reg query "HKLM\Software\Policies\Microsoft\Windows Defender"
```