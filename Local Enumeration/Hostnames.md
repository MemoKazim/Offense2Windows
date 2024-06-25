```
$activeHosts | ForEach-Object { 
	$hostname = (Resolve-DnsName -Name $_).NameHost 
	[PSCustomObject]@{ 
	IPAddress = $_ Hostname = $hostname 
	} 
} | Format-Table -AutoSize
```
-- output

	IPAddress     Hostname
	172.16.128.01        dc
