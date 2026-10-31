# Windows-Bereitstellung

## Windows-Bereitstellungsdienste

Auf dem `DC` wurden die Windows-Bereitstellungsdienste einschließlich der Verwaltungswerkzeuge installiert.

```powershell
Install-WindowsFeature WDS -IncludeManagementTools
```

## Installierte Komponenten

Die installierten Komponenten wurden mit PowerShell geprüft:

```powershell
Get-WindowsFeature WDS* |
Format-Table Name,InstallState -AutoSize
```

Installiert wurden:

- `WDS`
- `WDS-Deployment`
- `WDS-Transport`
- `WDS-AdminPack`

Damit sind die benötigten Serverrollen und Verwaltungswerkzeuge für die weitere Einrichtung der Windows-Bereitstellungsdienste vorhanden.
