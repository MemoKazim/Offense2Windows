### Network shares

> Enumerating shared folders and their permissions ensures that there might be sensitive information leak within network.

Get all Network shared objects

```cmd
net share
```

```Powershell
Get-SmbShare | select ShareState, Name, Path | ft
```


Get permission of Network Shared items

```Powershell
Get-SmbShare | foreach { Get-SmbShareAccess -Name $_.Name }
```


### Local file/folder permissions

>  Misconfigured file and folder permissions may lead to data breach

Get current access of the specified folder or file in local host 

``` Powershell
(Get-ACL <PATH>).access | ft IdentityReference,FileSystemRights,AccessControlType,IsInherited,InheritanceFlags -Auto -Wrap
```

Get file/folder owner of specified path

```Powershell
Get-ACL <PATH> | select Owner, Group, PSChildName
```

Recursively:

```Powershell
Get-ChildItem -Recurse -Force <PATH> | ForEach-Object { $path = $_.FullName; $acl = Get-Acl $path; $acl.Access | Where-Object { $_.IdentityReference -eq "$([System.Security.Principal.WindowsIdentity]::GetCurrent().Name)" -and ($_.FileSystemRights -match "FullControl") } | Select-Object @{Name='Path';Expression={$path}}, IdentityReference, FileSystemRights }
```
You can change "FullControl" with [following parameters](https://learn.microsoft.com/en-us/dotnet/api/system.security.accesscontrol.filesystemrights?view=net-8.0)

