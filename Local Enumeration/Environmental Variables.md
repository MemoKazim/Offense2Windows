>Environmental variables might contain sensitive information such as API keys

### Get-ChildItem

**Example Usage**

``` Powershell
Get-ChildItem env:*

ls env:*
```


**Output:**

``` Output
Name                           Value
----                           -----
SystemDrive                    C:
ProgramFiles(x86)              C:\Program Files (x86)
ProgramW6432                   C:\Program Files
PROCESSOR_IDENTIFIER           Intel64 Family 6 Model 151 Stepping 2, GenuineIntel
VBOX_MSI_INSTALL_PATH          C:\Program Files\Oracle\VirtualBox\
PROCESSOR_ARCHITECTURE         AMD64
Path                           C:\Program Files\Common                 Files\Oracle\Java\javapath;C:\Program Files (x86)\Common File...
PROCESSOR_REVISION             9702
CommonProgramFiles(x86)        C:\Program Files (x86)\Common Files
STARSHIP_SHELL                 powershell
WT_SESSION                     1229ba24-8cfd-4afc-ae66-94845bed5bc2
SystemRoot                     C:\Windows
CommonProgramFiles             C:\Program Files\Common Files
ZES_ENABLE_SYSMAN              1
WT_PROFILE_ID                  {61c54bbd-c2c6-5271-96e7-009a87ff44bf}
ProgramData                    C:\ProgramData
ALLUSERSPROFILE                C:\ProgramData
CommonProgramW6432             C:\Program Files\Common Files
VIRTUAL_ENV_DISABLE_PROMPT     1
PT8HOME                        C:\Program Files\Cisco Packet Tracer 8.2.1
SESSIONNAME                    Console
DriverData                     C:\Windows\System32\Drivers\DriverData
windir                         C:\Windows
NUMBER_OF_PROCESSORS           20
OS                             Windows_NT
ProgramFiles                   C:\Program Files
ComSpec                        C:\Windows\system32\cmd.exe
HOMEDRIVE                      C:
PATHEXT                        .COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC;.CPL
PROCESSOR_LEVEL                6
PUBLIC                         C:\Users\Public
```


### Registry

**Example Usage:**

``` powershell
reg query "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Environment"

reg query "HKCU\Environment"
```

