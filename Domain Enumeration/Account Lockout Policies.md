> List all the domain controllers in the Active Directory setup.
### Powershell

**Example Usage:**

``` Powershell
(Get-ADDefaultDomainPasswordPolicy).LockoutDuration
```

**Output:**

``` Output
Days              : 0
Hours             : 0
Minutes           : 1
Seconds           : 0
Milliseconds      : 0
Ticks             : 600000000
TotalDays         : 0.000694444444444444
TotalHours        : 0.0166666666666667
TotalMinutes      : 1
TotalSeconds      : 60
TotalMilliseconds : 60000
```

**Example Usage:**

``` Powershell
(Get-ADDefaultDomainPasswordPolicy).LockoutObservationWindow
```

**Output:**

``` Output
Days              : 0
Hours             : 0
Minutes           : 1
Seconds           : 0
Milliseconds      : 0
Ticks             : 600000000
TotalDays         : 0.000694444444444444
TotalHours        : 0.0166666666666667
TotalMinutes      : 1
TotalSeconds      : 60
TotalMilliseconds : 60000
```

**Example Usage:**

``` Powershell
(Get-ADDefaultDomainPasswordPolicy).LockoutThreshold
```

**Output:**

``` Output
0
```

### CMD

**Example Usage:**

``` cmd
net accounts /domain | findstr /i "Lockout Threshold Lockout Duration Lockout Observation Window"
```

**Output:**

``` Output
Lockout threshold:                                    Never
Lockout duration (minutes):                           1
Lockout observation window (minutes):                 1
```
