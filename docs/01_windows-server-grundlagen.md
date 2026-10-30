# Windows Server Grundlagen

## Systemübersicht

Der Server wurde über PowerShell geprüft. Dabei wurden Windows-Version und Hostname ermittelt.

```powershell
Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion, CsName
```

![Windows-Version und Hostname](../images/windows-version-hostname.png)

## Netzwerkprüfung

Die Erreichbarkeit des Standardgateways und die DNS-Namensauflösung wurden erfolgreich geprüft.

```powershell
Test-NetConnection 10.100.34.254
Resolve-DnsName lab.local
```

![Netzwerk- und DNS-Test](../images/netzwerk-dns-test.png)
