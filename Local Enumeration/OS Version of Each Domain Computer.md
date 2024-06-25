```
# Ensure the Active Directory module is imported
Import-Module ActiveDirectory

# Retrieve all computer objects and select necessary properties
$computers = Get-ADComputer -Filter * -Property Name, OperatingSystem, OperatingSystemVersion, OperatingSystemServicePack

# Format the output and display it
$computers | Select-Object Name, OperatingSystem, OperatingSystemVersion, OperatingSystemServicePack | Format-Table -AutoSize

```

```
Name        OperatingSystem                OperatingSystemVersion OperatingSystemServicePack
----        ---------------                ---------------------- --------------------------
DC          Windows Server 2019 Datacenter 10.0 (17763)                                     
FILE        Windows Server 2019 Datacenter 10.0 (17763)                                     
cl-01       Windows 10 Education           10.0 (19044)                                     
cl-02                                                                                       
cl-03       Windows 10 Enterprise          10.0 (19042)                                     
cl-04                                                                                       
cl-05                                                                                       
cl-06                                                                                       
cl-07                                                                                       
cl-08                                                                                       
cl-09                                                                                       
cl-10                                                                                       
cl-11                                                                                       
COMMANDO    Windows 10 Pro                 10.0 (19044)                                     
cl-13                                                                                       
cl-14                                                                                       
cl-15                                                                                       
cl-16                                                                                       
cl-17                                                                                       
cl-18                                                                                       
cl-19                                                                                       
cl-20                                                                                       
cl-21                                                                                       
cl-22       Windows 10 Education           10.0 (19044)                                     
cl-23                                                                                       
cl-24                                                                                       
cl-25                                                                                       
cl-26                                                                                       
cl-27                                                                                       
cl-28                                                                                       
cl-29                                                                                       
cl-30                                                                                       
cl-31                                                                                       
cl-32                                                                                       
cl-33                                                                                       
cl-34                                                                                       
cl-35                                                                                       
cl-36                                                                                       
cl-37                                                                                       
cl-38                                                                                       
cl-39                                                                                       
cl-40                                                                                       
cl-41                                                                                       
cl-42                                                                                       
cl-43                                                                                       
cl-44                                                                                       
cl-45                                                                                       
cl-46                                                                                       
cl-47                                                                                       
cl-48                                                                                       
cl-49                                                                                       
cl-50                                                                                       
cl-51                                                                                       
cl-52                                                                                       
cl-53                                                                                       
cl-54                                                                                       
cl-55                                                                                       
cl-56                                                                                       
cl-57                                                                                       
cl-58                                                                                       
cl-59                                                                                       
cl-60                                                                                       
cl-61                                                                                       
cl-62                                                                                       
cl-63                                                                                       
cl-64                                                                                       
cl-65                                                                                       
cl-66                                                                                       
cl-67                                                                                       
cl-68                                                                                       
cl-69                                                                                       
cl-70                                                                                       
cl-71                                                                                       
cl-72                                                                                       
cl-73                                                                                       
cl-74                                                                                       
cl-75                                                                                       
cl-76                                                                                       
cl-77                                                                                       
cl-78                                                                                       
cl-79                                                                                       
cl-80                                                                                       
cl-81                                                                                       
cl-82                                                                                       
cl-83                                                                                       
cl-84                                                                                       
cl-85                                                                                       
cl-86                                                                                       
cl-87                                                                                       
cl-88                                                                                       
cl-89                                                                                       
cl-90                                                                                       
cl-91                                                                                       
cl-92                                                                                       
cl-93                                                                                       
cl-94                                                                                       
cl-95                                                                                       
cl-96                                                                                       
cl-97                                                                                       
cl-98                                                                                       
cl-99                                                                                       
cl-100                                                                                      
cl-101                                                                                      
cl-102                                                                                      
cl-103                                                                                      
cl-104                                                                                      
cl-105                                                                                      
cl-106                                                                                      
cl-107                                                                                      
cl-108                                                                                      
cl-109                                                                                      
cl-110                                                                                      
cl-111                                                                                      
GYD-DC-01                                                                                   
GYD-FILE-01                                                                                 
GYD-DNS-01                                                                                  
CL-00       Windows 10 Enterprise          10.0 (10240)                                     
SVR-01      Windows Server 2019 Datacenter 10.0 (17763)                                     
SVR-02      Windows Server 2019 Datacenter 10.0 (17763)                                     


```