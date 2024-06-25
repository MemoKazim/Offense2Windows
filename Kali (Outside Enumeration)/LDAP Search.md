>Built-in interface for interacting with the LDAP protocol.

``` zsh
ldapsearch -x -b <DN / Search Base> -p <PORT> -H ldap://<IP>
```

``` zsh
ldapsearch -x -b <DN / Search Base> -H ldap://<IP> -W <LDAP QUERY>
```

## LDAP Query Syntax
### To match a single attribute

``` LDAP
(sAMAccountName=<SomeAccountName>)
```

### To match two attributes (and)

``` LDAP
(&(objectClass=<person>)(objectClass=<user>))
```

### To match two attributes (or)

``` LDAP
(|(objectClass=<person>)(objectClass=<user>))
```

### To match three attributes (and)

``` LDAP
(&(objectClass=<user>)(objectClass=<top>)(objectClass=<person>))
```

### To match three attributes (or)

``` LDAP
(!(objectClass=<user>)(objectClass=<top>)(objectClass=<person>))
```

### To perform a wildcard search

``` LDAP
(&(objectClass=<user>)(cn=<*Marketing*>))
```


## LDAP Account Filtering

### Domain and Enterprise Admins

``` LDAP
(objectClass=user)(objectCategory=Person)(adminCount=1)
```

### All users except blocked

``` LDAP
(objectCategory=person)(objectClass=user)(!userAccountControl:1.2.840.113556.1.4.803:=2)
```

### Disabled user accounts

``` LDAP
(objectCategory=person)(objectClass=user)(userAccountControl:1.2.840.113556.1.4.803:=16)
```

### Users with password never expires enabled

``` LDAP
(objectCategory=user)(userAccountControl:1.2.840.113556.1.4.803:=65536)
```
### Users in Department

``` LDAP
(&(objectCategory=person)(objectClass=user)(department=<Sales>))
```

### Exclude disabled users

To find as user (`sAMAccountName=<username>`) that isn't disabled:

``` LDAP
(&(objectCategory=person)(objectClass=user)(sAMAccountType=805306368)(!(userAccountControl:1.2.840.113556.1.4.803:=2))(sAMAccountName=<username>))
```
