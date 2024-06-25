>Great Tool for password / hash cracking

### NTLM Cracking

``` zsh
hashcat -m 1000 -a 0 -o <OUTPUT FILE> <HASH FILE> <PASSWORD WORDLIST>
```


### KRB5ASREP Cracking

``` zsh
hashcat -m 18200 <HASH> <WORDLIST>
```


### KRB5TGS Cracking

``` zsh
hashcat -m 13100 --force <TGS_TICKET> <WORDLIST>
```