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
