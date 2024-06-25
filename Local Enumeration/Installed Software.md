``` 
Get-WmiObject -Class Win32_Product | Select-Object -Property Name, Version 
```
```
Get-ItemProperty -Path 'HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\*' | Select-Object -Property DisplayName, DisplayVersion**
```

![[Pasted image 20240529222827.png]]