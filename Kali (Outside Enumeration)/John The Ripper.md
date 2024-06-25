>Great tool for offline password / hash cracking 

### NTLM Cracking

``` zsh
john --format=lm --wordlist=<WORDLIST> <NTLM_HASH>
```

### KRB5TGS Cracking

``` zsh
john --format=krb5tgs --wordlist=<WORDLIST> <TGS_TICKET>
```
