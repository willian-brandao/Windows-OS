# Arquivo de sistemas

Arquivos de Programas: Para programas 64 bit no windows 64 bits

Arquivos de Programas(x86): Para programas 32 bits

ProgramData: Programas para usuários independentes

\users: contém o diretório para casa usuário 

\public: para arquivos compartilhados

[username]\AppData: para dados e configurações de aplicativos por usuário

\windows: contém o sistema operacional

\system32: contém os principais componentes do windows e as bibliotecas de links dinâmicos

\winSxS: loja de componentes do windows (incluindo atualizações e service packs)

# File System

FAT ( File Allocation Table): Sistema de arquivos simples e compatível porém não suporta arquivos grandes (acima de 4GB) e não oferece funções de seguraça.

NTFS (New Technology File System): Projetado para lidar com as limitações do FAT. Ele suporta grandes arquivos, oferece funções de segurança avançadas como permissões de pastas e usa o espaço em disco mais eficientemente. É o sistema padrão do windows atual.

FAT32: Com a popularização dos pendrives, o FAT32 se tornou a solução ideal para os dispositivos de armazenamento. O  FAT32 é mais avançado que que o  FAT e suporta arquivos maiores que 4GB.

Com o sistema operacional windows vista, foi introduzido o exFAT (Extended File Allocation Table). Projetado para substituir o FAT32 e suportar arquivos maiores que 4GB. Embora não seja tão avançado quanto o NTFS, ele é mais simples e mais adequado para dispositivos de armazenamento portáteis. 

## NTFS e FAT

NTFS é conhecido como um sistema de arquivos de registro diário. Em um evento de falha, o sistema de arquivo podem automaticamente reparar pastas/aarquivos no disco usando as informações armazenadas no arquivo de registro. Essa feature não é possível no FAT. NTFS teve um significante desenvlvimento no momento que o armazenamento do Windows precisava crescer e superar várias limitações do FAT.

* Segurança - NTFS oferece um modelo de segurança mais robusto provendo permissões para controlar o acesso de arquivos.
* Escalabilidade - NTFS suporta arquivos grandes e capacidade de unidades maiores, acomodando necessidades de armazenamento mais modernas.
* Confiabilidade - NTFS provê registros para melhorar a integridade dos dados e recuperação.
* Funcionalidades - NTFS oferece funções adicionais como compressão de arquivos, encriptação e cotas de disco para melhorar o gerenciamento de armazenado e segurança.

# Lista de Controle de Acesso (ACL)

A lista determina quem pode acessar um recurso (arquivo, pasta, impressoras, recursos de redes) em um sistema de computador e o quais permissões a pessoa deve ter.

ACL permite que administradores de sistemas e usuários protejam dados sensíveis e assegurem que apenas pessoas autorizadas podem acessar recursos específicos.

No discos NTFS permissão de acesso para arquivos e pastas podem ser configurados.

As permissões ajustáveis são:
* Controle Total
* Modificar
* Ler e Executar
* Listas pastas e conteúdos
* Ler
* Escrever

# Controle de Contas de Usuários (UAC)

Uma funcionalidade de segurança embutida no sistema operacional. UAC trabalha requisitando confirmação antes de performar operações que requerem permissões administrativas no computador. Isso ajuda a prevenir erros causados por mudanças não autorizadas ou instalações de malwares. 

Quando um programa tenta executar uma operação que requer privilégios administrativos( instalar programas, mudar configurações de sistema), a janela do UAC aparece na tela e a ação deve ser aceita ou negada.

### Níveis

* Sempre notificar.
* Notificar somente quando programas tentam realizar mudanças no computador(padrão): apenas notificações de ações feitas por programas, mas não pelo próprio usuário.
* Notificar somente quando programas tentarem fazer alterações no meu computador: a área de trabalho permanece utilizável quando a janela do UAC está aberta.
* Nunca notificar.





  
  



  
