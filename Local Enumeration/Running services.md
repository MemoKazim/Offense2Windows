>Some services might contain vulnerability such as *Unquoted Path*

### Get-Service

**Example:**

``` Powershell
# Get all running services
$runningServices = Get-Service | Where-Object { $_.Status -eq 'Running' }

# Output running services
Write-Host "Running Services:" -ForegroundColor Cyan
$runningServices | ForEach-Object {
    Write-Host "Service Name: $($_.Name), Display Name: $($_.DisplayName), Status: $($_.Status)"
}

```


**Output:**

``` Output
Running Services:
Service Name: ADWS, Display Name: Active Directory Web Services, Status: Running
Service Name: AppMgmt, Display Name: Application Management, Status: Running
Service Name: BFE, Display Name: Base Filtering Engine, Status: Running
Service Name: BrokerInfrastructure, Display Name: Background Tasks Infrastructure Service, Status: Running
Service Name: BthAvctpSvc, Display Name: AVCTP service, Status: Running
Service Name: CDPSvc, Display Name: Connected Devices Platform Service, Status: Running
Service Name: CDPUserSvc_b4bfc, Display Name: Connected Devices Platform User Service_b4bfc, Status: Running
Service Name: CertPropSvc, Display Name: Certificate Propagation, Status: Running
Service Name: COMSysApp, Display Name: COM+ System Application, Status: Running
Service Name: CoreMessagingRegistrar, Display Name: CoreMessaging, Status: Running
Service Name: CryptSvc, Display Name: Cryptographic Services, Status: Running
Service Name: DcomLaunch, Display Name: DCOM Server Process Launcher, Status: Running
Service Name: Dfs, Display Name: DFS Namespace, Status: Running
Service Name: DFSR, Display Name: DFS Replication, Status: Running
Service Name: Dhcp, Display Name: DHCP Client, Status: Running
Service Name: DiagTrack, Display Name: Connected User Experiences and Telemetry, Status: Running
Service Name: DNS, Display Name: DNS Server, Status: Running
Service Name: Dnscache, Display Name: DNS Client, Status: Running
Service Name: DPS, Display Name: Diagnostic Policy Service, Status: Running
Service Name: DsSvc, Display Name: Data Sharing Service, Status: Running
Service Name: EventLog, Display Name: Windows Event Log, Status: Running
Service Name: EventSystem, Display Name: COM+ Event System, Status: Running
Service Name: FontCache, Display Name: Windows Font Cache Service, Status: Running
Service Name: gpsvc, Display Name: Group Policy Client, Status: Running
Service Name: IKEEXT, Display Name: IKE and AuthIP IPsec Keying Modules
```


### Get-WmiObject

**Example:**

``` Powershell
Get-WmiObject win32_service | Select Name, DisplayName, State, PathName | Sort PathName
```

By getting Services execution path name you can define whether there are *Unquoted Path Vulnerability* in remote server