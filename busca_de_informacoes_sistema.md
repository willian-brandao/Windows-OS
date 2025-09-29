# Comandos 

## Buscar informações sobre o sistema operacional
```
PS C:\Users\Administrator> Get-ComputerInfo

WindowsBuildLabEx                                       : 17763.1.amd64fre.rs5_release.180914-1434
WindowsCurrentVersion                                   : 6.3
WindowsEditionId                                        : ServerStandard
WindowsInstallationType                                 : Server
WindowsInstallDateFromRegistry                          : 3/20/2024 4:48:20 AM
WindowsProductId                                        : 00429-00000-00001-AA815
WindowsProductName                                      : Windows Server 2019 Standard
```

```
PS C:\Users\Administrator> Get-WmiObject -Class win32_OperatingSystem

SystemDirectory : C:\Windows\system32
Organization    :
BuildNumber     : 17763
RegisteredUser  : Windows User
SerialNumber    : 00429-00000-00001-AA815
Version         : 10.0.17763
```
## Mostrar todos os updates instalados
```
PS C:\Users\Administrator> Get-Hotfix

Source        Description      HotFixID      InstalledBy          InstalledOn
------        -----------      --------      -----------          -----------
SRV2019       Update           KB4464455                          10/29/2018 12:00:00 AM
```
## Mostrar as funcionalidades do Defender
```
PS C:\Users\Administrator> Get-Service | Where-Object DisplayName -like '*Defender*'

Status   Name               DisplayName
------   ----               -----------
Running  mpssvc             Windows Defender Firewall
Stopped  Sense              Windows Defender Advanced Threat Protection
Running  WdNisSvc           Windows Defender Antivirus Network Inspection Service
Running  WinDefend          Windows Defender Antivirus Service
```
## Buscar por textos em arquivos
```
Get-ChildItem -Recurse *.* | Select-String -Pattern "SEARCH_STR"
```

## Visualizar as permissões de arquivos ou pastas
```
Get-Acl file.txt
```
## Acessar o hash de arquivos
```
Get-FileHash file.txt
```

