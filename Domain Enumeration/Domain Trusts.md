>Understanding the relationship between different domain may give you ability to move between different domains within organization

### Get-ADTrust

``` Powershell
Get-ADTrust -Filter *
```

**Advantages:**

·         Lists all trust relationships in the domain.
·         Provides detailed information about each trust.
·         Can filter and format output as needed.


**Example Usage:**

``` Powershell
Get-ADTrust -Filter * | Format-Table Name, Source, Target, TrustType, TrustDirection, TrustAttributes
```


**Possible Output:**

| Name               | Source            | Target             | TrustType   | TrustDirection | TrustAttributes |
| ------------------ | ----------------- | ------------------ | ----------- | -------------- | --------------- |
| example.com/trust1 |     example.com   | trust1.example.com | Forest      | Bidirectional  | 0               |
| example.com/trust2 | example.com       | trust2.example.com | External    | Outbound       | 1               |
| example.com/trust3 | example.com       | trust3.example.com | ParentChild | Bidirectional  | 0               |

### nltest

``` cmd
nltest /domain_trusts
```

**Advantages:**

·         Simple and quick way to list all domain trusts.
·         Does not require administrative privileges on the domain.

**Example Usage:**

``` cmd
nltest /domain_trusts
```

**Possible Output:**

| Flags | 30 HAS_TDO | TRUSTED                    |
| ----- | ---------- | -------------------------- |
| 0     | TRUSTED    | example.com (NT 5)         |
| 1     | TRUSTED    | trust1.example.com (MIT)   |
| 2     | INBOUND    |  trust2.example.com (NT 5) |
_______________
