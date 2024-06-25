>Identifying domain controllers is essential for understanding AD Infrastructure

### Get-ADDomainController

``` Powershell
Get-ADDomainController
```

```Powershell
Get-ADDomainController -Filter *
```

**Advantages:**

·         Lists all domain controllers in the domain.
·         Provides detailed information about each domain controller.
·         Can filter and format output as needed.

**Example Usage:**

```Powershell
Get-ADDomainController -Filter * | Format-Table Name, IPv4Address, Site, OperatingSystem
```

**Possible Output:**

| Name | IPv4Address  | Site                    | OperatingSystem              |
| ---- | ------------ | ----------------------- | ---------------------------- |
| DC1  | 192.168.1.10 | Default-First-Site-Name | Windows Server 2016 Standard |
| DC2  | 192.168.1.11 | Default-First-Site-Name | Windows Server 2019 Standard |
| DC3  | 192.168.1.12 | RemoteSite              | Windows Server 2016 Standard |

### Get-ADComputer

``` Powershell
Get-ADComputer -Filter {OperatingSystem -Like "*Windows Server*"} -Property Name, OperatingSystem | Where-Object { $_.OperatingSystem -match "Domain Controller" }
```

**Example Usage:**

``` Powershell
Get-ADComputer -Filter {OperatingSystem -Like "*Windows Server*"} -Property Name, OperatingSystem | Where-Object { $_.OperatingSystem -match "Domain Controller" } | Select-Object Name, OperatingSystem
```

**Possible Output:**

| Name | OperatingSystem                  |
| ---- | -------------------------------- |
| DC1  | Windows Server 2016 Standard     |
| DC2  | Windows Server 2019 Standard<br> |
| DC3  | Windows Server 2016 Standard     |
          