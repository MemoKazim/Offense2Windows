> Monitor the replication status and overall health of the Active Directory environment.
### CMD

**Example Usage:**

``` cmd
repadmin /showrepl /errorsonly
```

**Output:**

``` Output
Repadmin: running command /showrepl against full DC localhost
Default-First-Site-Name\DC
DSA Options: IS_GC
Site Options: (none)
DSA object GUID: 4396d0fa-4f43-4c92-880e-f4ba7c62038d
DSA invocationID: 973ddb65-286c-4a99-8ee6-342bb3672394
```

**Example Usage:**

``` cmd
repadmin /replsummary
```

**Output:**

``` Output
Replication Summary Start Time: 2024-05-30 08:00:00

Beginning data collection for replication summary, this may take awhile:

Source DSA          largest delta    fails/total %%   error
---------------------------------------------------
DC1.example.com      15m:32s         0 / 10    0
DC2.example.com      20m:11s         0 / 10    0

Destination DSA     largest delta    fails/total %%   error
---------------------------------------------------
DC3.example.com      10m:25s         0 / 10    0
DC4.example.com      18m:47s         0 / 10    0

Summary: Outbound replication finished successfully. Errors: 0. Replication latency: 0 hours, 20 minutes, and 10 seconds.
```