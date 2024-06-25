> Examine the DNS zones and records associated with Active Directory.
### Script

**Example Usage:**

``` Powershell
Import-Module DnsServe
$zones = Get-DnsServerZone
foreach ($zone in $zones) {
    Write-Host "Zone: $($zone.ZoneName)"
    $records = Get-DnsServerResourceRecord -ZoneName $zone.ZoneName
    $records | Select-Object -Property HostName, RecordType, RecordClass, TimeToLive, RecordData
    Write-Host ""
}
```

**Output:**

``` Output
HostName    : @
RecordType  : NS
RecordClass : IN
TimeToLive  : 01:00:00
RecordData  : DnsServerResourceRecordNS

HostName    : @
RecordType  : SOA
RecordClass : IN
TimeToLive  : 01:00:00
RecordData  : DnsServerResourceRecordSoa

HostName    : 4396d0fa-4f43-4c92-880e-f4ba7c62038d
RecordType  : CNAME
RecordClass : IN
TimeToLive  : 00:10:00
RecordData  : DnsServerResourceRecordCName

HostName    : _kerberos._tcp.Default-First-Site-Name._sites.dc
RecordType  : SRV
RecordClass : IN
TimeToLive  : 00:10:00
RecordData  : DnsServerResourceRecordSrv
```

**Example Usage:**

``` Powershell
Import-Module DnsServer
$zones = Get-DnsServerZone
$zones | Select-Object -Property ZoneName
```

**Output:**

``` Output
ZoneName        
--------        
_msdcs.acc.lab  
0.in-addr.arpa  
127.in-addr.arpa
255.in-addr.arpa
acc.lab         
TrustAnchors
```
### CMD

**Example Usage:**

``` cmd
dnscmd /enumzones
```

**Output:**

``` Output
Enumerated zone list:
        Zone count = 4

 Zone name                      Type       Storage         Properties

 .                              Cache      AD-Domain
 _msdcs.acc.lab                 Primary    AD-Forest       Secure
 acc.lab                        Primary    AD-Domain       Secure
 TrustAnchors                   Primary    AD-Forest


Command completed successfully.
```
