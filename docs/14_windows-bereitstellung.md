# Windows-Bereitstellung

## Status

Auf dem `DC` wurden die Komponenten der Windows-Bereitstellungsdienste installiert.

```powershell
Get-WindowsFeature WDS* |
Format-Table Name,InstallState -AutoSize
```

Installiert wurden:

- `WDS`
- `WDS-Deployment`
- `WDS-Transport`
- `WDS-AdminPack`

## Einschränkung

Die Initialisierung des Bereitstellungsservers konnte in der vorhandenen Laborumgebung nicht abgeschlossen werden.

```powershell
wdsutil /Initialize-Server /RemInst:"C:\RemoteInstall"
```

Der Vorgang wurde mit dem Fehlercode `0x2` beendet. Zusätzlich waren die für die weitere Konfiguration vorgesehenen Installationsmedien für `MDT`, `ADK`, `WinPE` und `LiteTouchPE_x64.iso` nicht verfügbar.

Daher wurden keine Boot- oder Installationsabbilder hinzugefügt und keine Windows-Bereitstellung durchgeführt.
