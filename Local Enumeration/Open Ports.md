```
Get-NetTCPConnection | Where-Object {$_.State -eq "Listen"}
$netstatListening 
```
![[Pasted image 20240529214832.png]]