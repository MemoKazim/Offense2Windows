>By understanding AD replication, Authentication boundaries and AD site & subnets you can cause replication issues
## Get-ADReplicationSite

**Example usage**

``` Powershell
Get-ADReplicationSite
```

``` Powershell
Get-ADReplicationSite -Filter * | ForEach-Object { $_; Get-ADReplicationSubnet -Filter {Site -eq $_.Name} } | ft
```

**Advantages:**

·         Provides detailed information about AD sites.
·         Lists subnets associated with each site.
·         Can format and filter output as needed.

## nltest

**Example usage**

``` Powershell
nltest /dsgetsite
```


**Possible Output:**

```
Default-First-Site-Name
------------------------
The command completed successfully
```