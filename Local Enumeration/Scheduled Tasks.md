` SCHTASKS /Query /FO LIST /V  `


![[Pasted image 20240529221528.png]]

` Get-ScheduledTask | Select-Object TaskName, TaskPath, State `

![[Pasted image 20240529221732.png]]

