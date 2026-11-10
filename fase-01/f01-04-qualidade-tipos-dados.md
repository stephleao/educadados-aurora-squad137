# F01-04 — Qualidade e tipos de dados

As **11 tabelas** foram inspecionadas no Google Sheets e tiveram seus tipos conferidos na importação pelo Power Query. Colunas de data foram convertidas para Data; campos Sim/Não, para Lógico (`true/false`). **Nenhum erro foi identificado nas inspeções realizadas.**

| Tabela | Ajuste ou decisão |
|---|---|
| `calendario` | Reimportada sem a conversão automática incorreta; tipos definidos manualmente. Nulos em campos de feriado mantidos por serem legítimos. |
| `filiais` | Removidas linhas completamente vazias. Nulos em `data_encerramento` mantidos para filiais ativas. |
| `metas_valor` e `metas_quantidade` | Nulos nas chaves de entidades preservados quando decorrentes do preenchimento conforme o campo `nivel`. |

**Resultado registrado:** tipos revisados, linhas inteiramente vazias removidas e nulos esperados preservados. Dados preparados para modelagem.
