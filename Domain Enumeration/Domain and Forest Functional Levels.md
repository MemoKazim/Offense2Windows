>Lower function level may lack critical security features
### Get-ADDomain

**Example usage**

``` Powershell
Get-ADDomain | Select-Object, DomainMode
```

**Advantages:**

·         Quickly retrieves the functional level of the current domain.
·         Provides a clear output of the domain's functional level.


**Possible Output:**

```Output
DomainMode
----------
Windows2016Domain
```

### Get-ADForest

**Example Usage**

``` Powershell
Get-ADForest | Select-Object ForestMode
```

**Advantages:**

·         Quickly retrieves the functional level of the forest.
·         Provides a clear output of the forest's functional level.


**Possible Output:**

```Output
ForestMode
----------
Windows2016Forest
```
