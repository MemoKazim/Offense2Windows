
```
# Retrieve all running processes
$runningProcesses = Get-Process

# Output running processes
Write-Host "Running Processes:" -ForegroundColor Cyan
foreach ($process in $runningProcesses) {
    Write-Host "Process ID: $($process.Id), Name: $($process.Name), CPU: $($process.CPU), Memory: $($process.MemoryUsage)"
}

```

```
Running Processes:
Process ID: 7048, Name: ApplicationFrameHost, CPU: 0.265625, Memory: 
Process ID: 236, Name: chrome, CPU: 0.0625, Memory: 
Process ID: 2272, Name: chrome, CPU: 16.3125, Memory: 
Process ID: 2304, Name: chrome, CPU: 48.671875, Memory: 
Process ID: 3220, Name: chrome, CPU: 0.6875, Memory: 
Process ID: 3988, Name: chrome, CPU: 7.96875, Memory: 
Process ID: 4280, Name: chrome, CPU: 0.296875, Memory: 
Process ID: 4848, Name: chrome, CPU: 8.71875, Memory: 
Process ID: 5552, Name: chrome, CPU: 2.09375, Memory: 
Process ID: 6564, Name: chrome, CPU: 2.15625, Memory: 
Process ID: 1260, Name: conhost, CPU: 0.890625, Memory: 
Process ID: 4080, Name: conhost, CPU: 1.9375, Memory: 
Process ID: 4608, Name: conhost, CPU: 11.3125, Memory: 
Process ID: 5532, Name: conhost, CPU: 0.15625, Memory: 
Process ID: 360, Name: csrss, CPU: , Memory: 
Process ID: 472, Name: csrss, CPU: , Memory: 
Process ID: 1516, Name: ctfmon, CPU: 2, Memory: 
Process ID: 3804, Name: dfsrs, CPU: , Memory: 
Process ID: 3096, Name: dfssvc, CPU: , Memory: 
Process ID: 732, Name: dllhost, CPU: 0.15625, Memory: 
Process ID: 4596, Name: dllhost, CPU: , Memory: 
Process ID: 3788, Name: dns, CPU: , Memory: 
Process ID: 384, Name: dwm, CPU: , Memory: 
Process ID: 5976, Name: explorer, CPU: 44.125, Memory: 
Process ID: 836, Name: fontdrvhost, CPU: , Memory: 
Process ID: 844, Name: fontdrvhost, CPU: , Memory: 
Process ID: 0, Name: Idle, CPU: , Memory: 
Process ID: 3852, Name: ismserv, CPU: , Memory: 
Process ID: 620, Name: lsass, CPU: , Memory: 
Process ID: 3764, Name: Microsoft.ActiveDirectory.WebServices, CPU: , Memory: 
Process ID: 6928, Name: mimikatz, CPU: 0.15625, Memory: 
Process ID: 3208, Name: msdtc, CPU: , Memory: 
Process ID: 1308, Name: powershell, CPU: 1.34375, Memory: 
Process ID: 4640, Name: powershell, CPU: 8.25, Memory: 
Process ID: 268, Name: powershell_ise, CPU: 131.328125, Memory: 
Process ID: 2100, Name: powershell_ise, CPU: 58.421875, Memory: 
Process ID: 88, Name: Registry, CPU: , Memory: 
Process ID: 2532, Name: RuntimeBroker, CPU: 0.75, Memory: 
Process ID: 4604, Name: RuntimeBroker, CPU: 2.375, Memory: 
Process ID: 5176, Name: RuntimeBroker, CPU: 0.453125, Memory: 
Process ID: 1368, Name: SearchUI, CPU: 5.5625, Memory: 
Process ID: 600, Name: services, CPU: , Memory: 
Process ID: 1204, Name: ShellExperienceHost, CPU: 2.21875, Memory: 
Process ID: 2564, Name: sihost, CPU: 1.28125, Memory: 
Process ID: 280, Name: smss, CPU: , Memory: 
Process ID: 3648, Name: spoolsv, CPU: , Memory: 
Process ID: 636, Name: svchost, CPU: , Memory: 
Process ID: 704, Name: svchost, CPU: , Memory: 
Process ID: 808, Name: svchost, CPU: , Memory: 
Process ID: 828, Name: svchost, CPU: , Memory: 
Process ID: 928, Name: svchost, CPU: , Memory: 
Process ID: 984, Name: svchost, CPU: , Memory: 
Process ID: 1048, Name: svchost, CPU: , Memory: 
Process ID: 1064, Name: svchost, CPU: , Memory: 
Process ID: 1112, Name: svchost, CPU: , Memory: 
Process ID: 1148, Name: svchost, CPU: , Memory: 
Process ID: 1164, Name: svchost, CPU: , Memory: 
Process ID: 1192, Name: svchost, CPU: , Memory: 
Process ID: 1252, Name: svchost, CPU: , Memory: 
Process ID: 1328, Name: svchost, CPU: , Memory: 
Process ID: 1348, Name: svchost, CPU: , Memory: 
Process ID: 1500, Name: svchost, CPU: , Memory: 
Process ID: 1588, Name: svchost, CPU: , Memory: 
Process ID: 1596, Name: svchost, CPU: , Memory: 
Process ID: 1608, Name: svchost, CPU: , Memory: 
Process ID: 1616, Name: svchost, CPU: , Memory: 
Process ID: 1624, Name: svchost, CPU: , Memory: 
Process ID: 1644, Name: svchost, CPU: , Memory: 
Process ID: 1672, Name: svchost, CPU: , Memory: 
Process ID: 1780, Name: svchost, CPU: 0.078125, Memory: 
Process ID: 1856, Name: svchost, CPU: , Memory: 
Process ID: 1876, Name: svchost, CPU: , Memory: 
Process ID: 1956, Name: svchost, CPU: , Memory: 
Process ID: 1964, Name: svchost, CPU: , Memory: 
Process ID: 2012, Name: svchost, CPU: , Memory: 
Process ID: 2020, Name: svchost, CPU: , Memory: 
Process ID: 2040, Name: svchost, CPU: 0.40625, Memory: 
Process ID: 2080, Name: svchost, CPU: , Memory: 
Process ID: 2236, Name: svchost, CPU: , Memory: 
Process ID: 2296, Name: svchost, CPU: , Memory: 
Process ID: 2312, Name: svchost, CPU: , Memory: 
Process ID: 2376, Name: svchost, CPU: , Memory: 
Process ID: 2480, Name: svchost, CPU: , Memory: 
Process ID: 2492, Name: svchost, CPU: , Memory: 
Process ID: 2528, Name: svchost, CPU: , Memory: 
Process ID: 2576, Name: svchost, CPU: , Memory: 
Process ID: 2808, Name: svchost, CPU: , Memory: 
Process ID: 2936, Name: svchost, CPU: , Memory: 
Process ID: 2972, Name: svchost, CPU: , Memory: 
Process ID: 3012, Name: svchost, CPU: , Memory: 
Process ID: 3112, Name: svchost, CPU: , Memory: 
Process ID: 3736, Name: svchost, CPU: , Memory: 
Process ID: 3756, Name: svchost, CPU: , Memory: 
Process ID: 3772, Name: svchost, CPU: , Memory: 
Process ID: 3780, Name: svchost, CPU: , Memory: 
Process ID: 3796, Name: svchost, CPU: , Memory: 
Process ID: 3844, Name: svchost, CPU: , Memory: 
Process ID: 3872, Name: svchost, CPU: , Memory: 
Process ID: 4084, Name: svchost, CPU: , Memory: 
Process ID: 5152, Name: svchost, CPU: , Memory: 
Process ID: 5184, Name: svchost, CPU: , Memory: 
Process ID: 5192, Name: svchost, CPU: , Memory: 
Process ID: 5424, Name: svchost, CPU: , Memory: 
Process ID: 5920, Name: svchost, CPU: , Memory: 
Process ID: 5988, Name: svchost, CPU: , Memory: 
Process ID: 6672, Name: svchost, CPU: , Memory: 
Process ID: 4, Name: System, CPU: , Memory: 
Process ID: 4300, Name: taskhostw, CPU: 0.1875, Memory: 
Process ID: 6240, Name: taskhostw, CPU: 0.140625, Memory: 
Process ID: 3812, Name: VGAuthService, CPU: , Memory: 
Process ID: 3744, Name: vm3dservice, CPU: , Memory: 
Process ID: 3936, Name: vm3dservice, CPU: , Memory: 
Process ID: 3820, Name: vmtoolsd, CPU: , Memory: 
Process ID: 5492, Name: vmtoolsd, CPU: 6.34375, Memory: 
Process ID: 464, Name: wininit, CPU: , Memory: 
Process ID: 532, Name: winlogon, CPU: , Memory: 
Process ID: 4448, Name: WmiPrvSE, CPU: , Memory:
```