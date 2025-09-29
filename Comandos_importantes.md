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

### Criar pastas
```
C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/15/2024  11:30 PM    <DIR>          .
03/15/2024  11:30 PM    <DIR>          ..
               0 File(s)              0 bytes
               2 Dir(s)  20,308,930,560 bytes free

C:\Users\user\Documents>mkdir newdir

C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:32 PM    <DIR>          .
03/18/2024  10:32 PM    <DIR>          ..
03/18/2024  10:32 PM    <DIR>          newdir
               0 File(s)              0 bytes
               3 Dir(s)  20,308,930,560 bytes free
```

### Deletar diretórios
```
C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:32 PM    <DIR>          .
03/18/2024  10:32 PM    <DIR>          ..
03/18/2024  10:32 PM    <DIR>          newdir
               0 File(s)              0 bytes
               3 Dir(s)  20,308,930,560 bytes free

C:\Users\user\Documents>rmdir newdir

C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:32 PM    <DIR>          .
03/18/2024  10:32 PM    <DIR>          ..
               0 File(s)              0 bytes
               2 Dir(s)  20,308,860,928 bytes free
```

### Copiar arquivos
```
C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:35 PM    <DIR>          .
03/18/2024  10:35 PM    <DIR>          ..
03/18/2024  10:35 PM                 0 test.txt
               1 File(s)              0 bytes
               2 Dir(s)  20,308,324,352 bytes free

C:\Users\user\Documents>copy test.txt test1.txt
        1 file(s) copied.

C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:36 PM    <DIR>          .
03/18/2024  10:36 PM    <DIR>          ..
03/18/2024  10:35 PM                 0 test.txt
03/18/2024  10:35 PM                 0 test1.txt
               2 File(s)              0 bytes
               2 Dir(s)  20,308,324,352 bytes free
```
### Mover arquivos
```
C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:36 PM    <DIR>          .
03/18/2024  10:36 PM    <DIR>          ..
03/18/2024  10:35 PM                 0 test.txt
03/18/2024  10:35 PM                 0 test1.txt
               2 File(s)              0 bytes
               2 Dir(s)  20,308,324,352 bytes free

C:\Users\user\Documents>move test.txt ..\Desktop
        1 file(s) moved.

C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:38 PM    <DIR>          .
03/18/2024  10:38 PM    <DIR>          ..
03/18/2024  10:35 PM                 0 test1.txt
               1 File(s)              0 bytes
               2 Dir(s)  20,308,176,896 bytes free
```
### Deletar arquivos
```
C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:38 PM    <DIR>          .
03/18/2024  10:38 PM    <DIR>          ..
03/18/2024  10:35 PM                 0 test1.txt
               1 File(s)              0 bytes
               2 Dir(s)  20,308,045,824 bytes free

C:\Users\user\Documents>del test1.txt

C:\Users\user\Documents>dir
 Volume in drive C has no label.
 Volume Serial Number is AE5B-68D3

 Directory of C:\Users\user\Documents

03/18/2024  10:39 PM    <DIR>          .
03/18/2024  10:39 PM    <DIR>          ..
               0 File(s)              0 bytes
               2 Dir(s)  20,308,045,824 bytes free
```


## Powershell

### Alias

Alias são nomes especiais no powershell que são usados para criar shortcuts para cmdlets, funções e scripts. Eles ajudam a trabalhar mais rápido fazendo comandos mais curtos e fáceis de escrever.
Ex: O comando cd pode ser usado para Set-Location cmdlet.
```
PS C:\Users\user> alias cd

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           cd -> Set-Location
```


### Checar a versão do powershel
```
PS C:\Users\user> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      5.1.19041.1237
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.19041.1237
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
```

### Buscar mais informações sobre um comando
```
Get-Help Get-Help
```
### Comando para listar todos os comandos, cmdlets, functions, filtros, scripts 

para validar o uso do comando descreva o comando abaixo 
```
Get-Help -Name Get-Command -Detailed
```

### Listar o conteúdo do diretório

```
Get-ChildItem
```
### Mudar de diretório

```
PS C:\Users\user> Set-Location .\Documents\
PS C:\Users\user\Documents>
```

### Criar um arquivo novo ou uma pasta
```
PS C:\Users\user\Documents> New-Item file.txt

PS C:\Users\user\Documents> New-Item -ItemType Directory logs

Get-Help New-Item -examples
```

### Remover arquivos
```
PS C:\Users\user\Documents> Remove-Item .\logs\
```
### Copiar arquivos
```
PS C:\Users\user\Documents> Copy-Item file.txt file1.txt
```
### Mover arquivos
```
PS C:\Users\user\Documents> Move-Item .\file1.txt ..\Desktop\
```

### Ler conteúdo do arquivo

```
PS C:\Users\user\Documents> Get-Content .\file.txt
```

### Acessar os processos do sistema operacional
```
PS C:\Users\user> Get-Process
```
### Parar processos
```
PS C:\Users\user> Stop-Process -Id 5432
```
### Iniciar um processo

```
PS C:\Users\user> Start-Service -Name Appinfo
```

### Instalar pacotes
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

# Comandos mais complexos no powershell

O pipe permite deixar os comandos do powershell mais completos e realizar mais funções do que as determinadas anteriormente pelo comando.

### Select-Object

Comando para especificar propriedades de objetos em uma coleção mostrando apenas as informações necessárias.
```
Get-Process | Select-Object ProcessName, Id
```

### Where_object 

Permite filtrar objetos baseados em critérios específicos. 
```
Get-Service | Where-Object Status -eq "Running"
```

### Operadores Comuns
* -eq: equals
* -ne: not equal
* -gt: greater than
* -ge: greater than or equal
* -lt: less than
* -le: less than or equal

### Select String 
É usado para procurar e selecionar linhas de texto in arquivos
```
PS C:\Users\user\Documents> Select-String -Pattern "today" .\file.txt

file.txt:1:The purpose of today's training is to defeat yesterday's understanding. - Miyamoto Musashi
```
