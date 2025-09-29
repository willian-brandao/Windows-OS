# Comandos

## Acessar configuração de usuários e grupos

## CMD

``
lusmgr
``
### Listar arquivos e pastas em determinado diretório
```
C:\Users\user>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user

03/18/2024  07:14 PM    <DIR>          .
03/18/2024  07:14 PM    <DIR>          ..
03/15/2024  11:30 PM    <DIR>          3D Objects
03/15/2024  11:30 PM    <DIR>          Contacts
03/18/2024  09:34 AM    <DIR>          Desktop
03/15/2024  11:30 PM    <DIR>          Documents
03/16/2024  09:55 AM    <DIR>          Downloads
03/15/2024  11:30 PM    <DIR>          Favorites
03/15/2024  11:30 PM    <DIR>          Links
03/15/2024  11:30 PM    <DIR>          Music
03/15/2024  11:30 PM    <DIR>          Pictures
03/15/2024  11:30 PM    <DIR>          Saved Games
03/15/2024  11:31 PM    <DIR>          Searches
03/15/2024  11:30 PM    <DIR>          Videos
               0 File(s)              0 bytes
              14 Dir(s)  20,309,082,112 bytes free

```

### Mudar de diretório
```
C:\Users\user>cd Documents

C:\Users\user\Documents>
```

## Powershell

## Instalar pacotes
```Powershell
winget search Microsoft.Powershell
Name               Id                           Version Source
---------------------------------------------------------------
PowerShell         Microsoft.PowerShell         7.4.1.0 winget
PowerShell Preview Microsoft.PowerShell.Preview 7.5.0.2 winget


C:\>winget install --id Microsoft.Powershell --source winget
Found PowerShell [Microsoft.PowerShell] Version 7.4.1.0
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
Downloading https://github.com/PowerShell/PowerShell/releases/download/v7.4.1/PowerShell-7.4.1-win-x64.msi
  ██████████████████████████████   103 MB /  103 MB
Successfully verified installer hash
Starting package install...
Successfully installed
```

### Linux Ubuntu
``
sudo snap install powershell --classic
``
### macOS
``
brew install powershell/tap/powershell
``

