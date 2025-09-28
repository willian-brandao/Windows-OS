# Alternate Data Streams (ADS) — Como criar e ler

**Resumo rápido:** Alternate Data Streams (ADS) são fluxos adicionais suportados pelo NTFS que permitem anexar dados “ocultos” a um arquivo usando a sintaxe `arquivo:streamname`. Úteis para metadados ou informações suplementares, porém podem ser abusados por malware — use com cuidado.

---

## Requisitos
- Sistema de arquivos: **NTFS** (ADS não funciona em FAT/exFAT).
- Permissões: acesso de leitura/escrita aos arquivos/paths em questão.
- Ferramentas: CMD, PowerShell, ou utilitários como `streams.exe` (Sysinternals).

---

## Criar/escrever um ADS

### CMD (prompt)

```cmd
echo texto secreto > arquivo.txt:segredo
```
### Powershel

```
Set-Content -Path .\arquivo.txt -Stream "segredo" -Value "conteúdo oculto"

```
### Criar um ADS com JSON
```

Set-Content -Path .\relatorio.pdf -Stream "metadata" -Value '{"autor":"Willian","rev":1}'

```
### Gravar binário (ex.: pequena payload) a partir de um arquivo
```
Get-Content -Path .\payload.bin -Encoding Byte -ReadCount 0 | Set-Content -Path .\documento.docx -Stream "payload" -AsByteStream
```
# Ler/visualizar um ADS

```CMD
more < arquivo.txt:segredo
```

### Mostra o conteúdo do stream segredo.

```PowerShell
Get-Content -Path .\arquivo.txt -Stream "segredo"
```

# Listar ADS em arquivos e pastas
```CMD (rápido)
dir /R
```

## Mostra, ao lado de cada arquivo, os streams alternativos presentes no diretório.

```PowerShell (recursivo)
Get-ChildItem -Path C:\pasta -Recurse -Force -File | ForEach-Object {
  Get-Item -Path $_.FullName -Stream * -ErrorAction SilentlyContinue
}
```

### Sysinternals (recomendado para varredura)
```
streams.exe -s C:\pasta — lista streams recursivamente (baixe do Sysinternals).
```
## Remover um ADS
```PowerShell
Remove-Item -Path .\arquivo.txt -Stream "segredo"
```
### Alternativa (sobrescrever com vazio)
```
Set-Content -Path .\arquivo.txt -Stream "segredo" -Value ""
Remove-Item -Path .\arquivo.txt -Stream "segredo"
```
