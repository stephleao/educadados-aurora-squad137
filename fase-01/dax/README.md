# Medidas DAX — Painel Aurora

Esta pasta reúne as medidas DAX documentadas durante a Fase 1, preservadas como referência para a continuidade do projeto pela Squad 137.

- `medidas-base.dax` — valor líquido, número de vendas, valor bruto e quantidade de itens.
- `metas.dax` — metas por nível e metas consolidadas por filial, cidade e rede.
- `indicadores.dax` — percentuais de atingimento, status, cores e rótulo combinado.
- `exibicao.dax` — medidas textuais para mostrar "sem meta" na tabela de serviços.

**Atenção:** as medidas dependem do modelo e do contexto de filtros do Power BI. Validar cada fórmula antes de reutilizar ou adaptar para a Fase 2, especialmente nos cortes de grupo de serviço e serviço.

A formatação condicional da tabela de serviços foi configurada nos visuais do PBIX, sem medidas DAX adicionais de cor.

Consultar [regras de negócio](../regras-de-negocio.md) e [fechamento da Fase 1](../fechamento-fase-01.md).
