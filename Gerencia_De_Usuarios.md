Powershell pode ser usado como uma ferramenta poderosa para gerenciar usuários e grupos no Windows e no Active Directory, possibilitanto criar e deletar contas de usuários, resetar senhas, gerenciar membros de grupos.

# Active Directory
É um serviço de diretório desenvolvido pela Microsoft e é um componente do sistema operacional windows server. Isso provê um banco de dados centralizado para todos os dispositivos que estiverem no domínio, como usuários, impressoras, aplicações e outros recursos na rede.

# RSAT (Short for Remote Server Administration Tools)
É uma tecnologia da Microsoft que permite gerenciar remotamente o Windows Server de um computador que roda o sistema operacional Windows. 

RSAT inclui várias ferramentas de gerenciamento usando ferramentas de uma interface gráfica, enquanto outras são oferecidas como powershell cmdlets.

## Instalação

* Abra o menu Iniciar.

* á para Configurações.

* Selecione Aplicativos.

* Clique em Aplicativos e recursos.

* No painel à direita, encontre "Recursos opcionais".

* Clique em "Adicionar um recurso".

* Na janela que abrir, pesquise por "RSAT".

* Selecione o resultado da pesquisa.

* Clique em "Instalar".

# Gerência de Usuários e Grupos

Listando usuários e grupos e as permissões que eles possuem é possível validar riscos potenciais para a segurança dos dispositivos. 

## Gerência de Usuários 

### Get-LocalUser
Buscar as informações de um determinado usuário.
```
PS C:\Windows\system32> Get-LocalUser

Name               Enabled Description
----               ------- -----------
Administrator      False   Built-in account for administering the computer/domain
DefaultAccount     False   A user account managed by the system.
Guest              False   Built-in account for guest access to the computer/domain
user               True
WDAGUtilityAccount False   A user account managed and used by the system for Windows Defender Application Guard scenarios.
```
### New-LocalUser
Criar um novo usuário local
```
PS C:\Windows\system32> New-LocalUser -Name "j.doe" -Password (ConvertTo-SecureString -String 'password123' -AsPlainText -Force)

Name  Enabled Description
----  ------- -----------
j.doe True
```
### Set-LocalUser
Mudar as propriedades de um usuário.
```
Set-LocalUser -Name "j.doe" -Description "This is a test user."
```
### Habilitar e desabilitar usuários
```
#desabilitar
Disable-LocalUser -Name "j.doe"
# habilitar
Enable-LocalUser -Name "j.doe"
```
### Remove-LocalUser
Deleta o usuário do computador
```
Remove-LocalUser -Name "j.doe"
```

## Gerência de Grupos

### Get-LocalGroup
Lista todos os grupos locais
```
Get-LocalGroup
```

### New-LocalGroup
Criar um novo grupo
```
New-LocalGroup -Name "Students"
```


