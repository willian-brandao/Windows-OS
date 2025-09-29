## Obter informações de endereço IP
```
Get-NetIPAddress
```
```
ipconfig
```
## netstat 
Mostra informações das conexões de redes para protocolos TCP/IP, tabelas de roteamento e interfaces de rede
```
netstat
```
## Nslookup
Ferramenta usada para consultar DNS para obter os nomes de domínios ou endereços de IP mapeados. 
```
PS C:\> nslookup example.com
Server:  localhost
Address:  ::1

Non-authoritative answer:
Name:    example.com
Addresses:  2606:2800:220:1:248:1893:25c8:1946
          93.184.216.34
```

## ARP
Protocolo usado para mapear endereços IP para endereços MAC em uma rede.
```
PS C:\> arp -a

Interface: 10.0.2.15 --- 0x6
  Internet Address      Physical Address      Type
  10.0.2.2              52-55-0a-00-02-02     dynamic
  10.0.2.3              52-55-0a-00-02-03     dynamic
  10.0.2.255            ff-ff-ff-ff-ff-ff     static
```

## Para testar o status da conexão de rede 

```
Test-NetConnection
```

## Baixar Arquivos
O comando Invoke-WebRequest é um cmdlet usado para interagir com serviços de páginas web. 
```
Invoke-WebRequest -Uri "https://upload.wikimedia.org/wikipedia/commons/a/af/PowerShell_Core_6.0_icon.png" -OutFile "powershell.png"
```
