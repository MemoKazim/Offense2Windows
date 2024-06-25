`netstat -ano`

![[Pasted image 20240529220224.png]]

```
**Get-NetTCPConnection | Select-Object -Property LocalAddress, LocalPort, RemoteAddress, RemotePort, State, OwningProcess |**

**ForEach-Object {**

    **$_ | Add-Member -MemberType NoteProperty -Name ProcessName -Value (Get-Process -Id $_.OwningProcess).Name**

    **$_**

**} | Format-Table -AutoSize
```

![[Pasted image 20240529220441.png]]

