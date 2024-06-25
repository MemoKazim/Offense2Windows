``` Powershell
# Retrieve all local users
$localUsers = Get-WmiObject -Class Win32_UserAccount -Filter "LocalAccount=True"

# Retrieve all local groups
$localGroups = Get-WmiObject -Class Win32_Group -Filter "LocalAccount=True"

# Function to get permissions for a given user or group
function Get-UserPermissions {
    param (
        [string]$UserName
    )
    $acl = Get-Acl -Path "C:\"
    $permissions = $acl.Access | Where-Object { $_.IdentityReference -match $UserName }
    return $permissions
}

# Output local users, their groups, and their permissions
Write-Host "Local Users, their Groups, and Permissions:" -ForegroundColor Cyan

foreach ($user in $localUsers) {
    Write-Host "User: $($user.Name) ($($user.FullName))" -ForegroundColor Yellow
    $userGroups = @()
    
    foreach ($group in $localGroups) {
        $members = Get-WmiObject -Query "Associators Of {Win32_Group.Domain='$($group.Domain)',Name='$($group.Name)'} Where AssocClass=Win32_GroupUser Role=PartComponent"
        foreach ($member in $members) {
            if ($member.PartComponent -like "*$($user.Name)*") {
                $userGroups += $group.Name
            }
        }
    }
    
    Write-Host "  Groups:"
    foreach ($group in $userGroups) {
        Write-Host "    - $group"
    }
    
    Write-Host "  Permissions:"
    $permissions = Get-UserPermissions -UserName $user.Name
    foreach ($permission in $permissions) {
        Write-Host "    - Path: $($permission.FileSystemRights), Access: $($permission.AccessControlType)"
    }
    
    Write-Host "" # Add a blank line for readability
}

```