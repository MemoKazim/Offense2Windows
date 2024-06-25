>  Catalog the configurations and certificate templates of Active Directory Certificate Services (AD CS).
### CMD

**Example Usage:**

``` cmd
certutil -view -restrict "Disposition=20" -out "RequestID,RequesterName,CertificateTemplate,OIDs,SerialNumber,NotBefore,NotAfter
```

**Output:**

``` Output
RequestID: 1234
RequesterName: CN=John Doe, OU=IT, O=Company, L=City, S=State, C=US
CertificateTemplate: WebServer
OIDs: 1.3.6.1.5.5.7.3.1, 1.3.6.1.4.1.311.21.10
SerialNumber: 12AB34CD56EF78GH90IJ12KL34MN56OP
NotBefore: 05/01/2024 08:00 AM
NotAfter: 05/01/2025 08:00 AM

RequestID: 1235
RequesterName: CN=Jane Smith, OU=Finance, O=Company, L=City, S=State, C=US
CertificateTemplate: User
OIDs: 1.3.6.1.5.5.7.3.2
SerialNumber: 34MN56OP78QR90ST12UV34WX56YZ78AB
NotBefore: 06/01/2024 09:00 AM
NotAfter: 06/01/2025 09:00 AM

RequestID: 1236
RequesterName: CN=Server01, OU=Servers, O=Company, L=City, S=State, C=US
CertificateTemplate: Machine
OIDs: 1.3.6.1.5.5.7.3.3, 1.3.6.1.4.1.311.20.2.2
SerialNumber: 56YZ78AB90CD12EF34GH56IJ78KL90MN
NotBefore: 07/01/2024 10:00 AM
NotAfter: 07/01/2025 10:00 AM

```
