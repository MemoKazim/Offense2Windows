>A tool written in Go that uses Kerberos Pre-Authentication to enumerate Active Directory accounts, perform password spraying, and brute-forcing.
### User enumeration

``` zsh
./kerbrute userenum -d <FQDN OF DOMAIN> <USERNAME WORDLIST>
```


### Password Spray

``` zsh
./kerbrute passwordspray -d <FQDN OF DOMAIN> <USERNAMES> <PASSWORD WORDLIST>
```

### Username Brute Force

``` zsh
./kerbrute bruteuser -d <FQDN OF DOMAIN> <PASSWORD WORDLIST> <USER>
```

