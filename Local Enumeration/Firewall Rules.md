>Misconfigured firewalls makes system vulnerable for unauthorized accesses

### Get-NetFirewallRule

**Example Usage:**

```Powershell
Get-NetFirewallRule | select Name, Group, Enabled, Profile, Direction, Action, Owner | sort Direction | ft
```

**Output**

``` Output
Name      : RVM-RPCSS-In-TCP
Group     : @FirewallAPI.dll,-34501
Enabled   : False
Profile   : Any
Direction : Inbound
Action    : Allow
Owner     :

Name      : FPS-NB_Session-Out-TCP
Group     : @FirewallAPI.dll,-28502
Enabled   : True
Profile   : Domain, Private, Public
Direction : Outbound
Action    : Allow
Owner     :

Name      : {E096F20F-4F7B-4147-97FA-65167A839257}
Group     : @{Microsoft.Windows.CloudExperienceHost_10.0.17763.1_neutral_neutral_cw5n1h2txyewy?ms-resource://Microsoft.Windows.CloudExperienceHost/resources/appDescription}
Enabled   : True
Profile   : Domain, Private
Direction : Inbound
Action    : Allow
Owner     : S-1-5-21-1485720640-942268468-2087739954-2214

Name      : {1435558B-0BEF-478C-92AB-F3EEC1B46831}
Group     : @{Microsoft.Windows.ShellExperienceHost_10.0.17763.1_neutral_neutral_cw5n1h2txyewy?ms-resource://Microsoft.Windows.ShellExperienceHost/resources/PkgDisplayName}
Enabled   : True
Profile   : Domain, Private, Public
Direction : Outbound
Action    : Allow
Owner     : S-1-5-21-1485720640-942268468-2087739954-2214
```

### Get-NetFirewallPortFilter

**Example Usage:**

``` Powershell
Get-NetFirewallPortFilter | Where-Object { $_.LocalPort -eq 5353 }


Get-NetFirewallPortFilter | Where-Object { $_.LocalPort -eq 5353 } | Get-NetFirewallRule | select *
```

**Output:**

``` Output
Protocol                : UDP
LocalPort               : 5353
RemotePort              : Any
IcmpType                : Any
DynamicTarget           : Any
DynamicTransport        : Any
Caption                 :
Description             :
ElementName             :
InstanceID              : MDNS-In-UDP-Domain-Active
CommunicationStatus     :
DetailedStatus          :
HealthState             :
InstallDate             :
Name                    :
OperatingStatus         :
OperationalStatus       :
PrimaryStatus           :
Status                  :
StatusDescriptions      :
CreationClassName       : MSFT|FW|FirewallRule|MDNS-In-UDP-Domain-Active
IsNegated               :
SystemCreationClassName :
SystemName              :
PSComputerName          :
CimClass                : root/standardcimv2:MSFT_NetProtocolPortFilter
CimInstanceProperties   : {Caption, Description, ElementName, InstanceID...}
CimSystemProperties     : Microsoft.Management.Infrastructure.CimSystemProperties

Protocol                : UDP
LocalPort               : 5353
RemotePort              : Any
IcmpType                : Any
DynamicTarget           : Any
DynamicTransport        : Any
Caption                 :
Description             :
ElementName             :
InstanceID              : MDNS-In-UDP-Public-Active
CommunicationStatus     :
DetailedStatus          :
HealthState             :
InstallDate             :
Name                    :
OperatingStatus         :
OperationalStatus       :
PrimaryStatus           :
Status                  :
StatusDescriptions      :
CreationClassName       : MSFT|FW|FirewallRule|MDNS-In-UDP-Public-Active
IsNegated               :
SystemCreationClassName :
SystemName              :
PSComputerName          :
CimClass                : root/standardcimv2:MSFT_NetProtocolPortFilter
CimInstanceProperties   : {Caption, Description, ElementName, InstanceID...}
CimSystemProperties     : Microsoft.Management.Infrastructure.CimSystemProperties

```

