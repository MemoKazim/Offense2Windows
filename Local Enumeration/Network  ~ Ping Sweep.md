` Perform a ping test for each IP address in the range
```
Define the range of IP addresses to scan
$ipRange = "192.168.1.1-254"


$results = 1..254 | ForEach-Object { Test-Connection -ComputerName "192.168.1.$_" -Count 1 -Quiet }

# Create an array to store the active hosts
$activeHosts = @()

# Iterate through the results and add active hosts to the array
for ($i = 0; $i -lt $results.Count; $i++) {
    if ($results[$i]) {
        $activeHosts += "192.168.1.$($i + 1)"
    }
}

# Display the active hosts and their IP addresses
$activeHosts | ForEach-Object { [System.Net.Dns]::GetHostEntry($_) } | Select-Object HostName, AddressList


PS C:\Users\duser> $ipRange = 1..254 | ForEach-Object {"192.168.100.$_"}
$ipRange | ForEach-Object {
    if (Test-Connection -ComputerName $_ -Count 1 -Quiet) {
        Write-Output "$_ is up"
    }
}
```
```
-- output
192.168.100.10 is up