# Fechamento da Fase 1 — Painel Aurora

**Entrega original:** 07/11/2026, por Stephanne Leão na squad anterior. **Registro de encerramento:** 09/11/2026. A Squad 137 também realizou sua entrega em 09/11/2026, conforme o [registro de entrega](../entregas/fase-01.md).

## Resultado entregue

Relatório comercial no Power BI, com duas páginas (**Visão Geral** e **Detalhamento**), incluindo vendas, metas e percentuais; gráficos de filial, cidades e grupos de serviço; matrizes de vendedores e profissionais; tabela de serviços; filtros de período, rótulos de valor e quantidade e formatação condicional.

As fórmulas estão em [DAX da Fase 1](dax/README.md). A indicação **"sem meta"** na tabela de serviços utiliza medidas textuais separadas das numéricas; a formatação condicional da tabela foi feita nos visuais.

## Limitação conhecida

Ao selecionar um grupo no gráfico de grupos de serviço, **o indicador percentual não atualizava como solicitado**. A causa não foi confirmada, e o problema não foi corrigido antes da entrega. A revisão futura deve considerar interações dos visuais, caminhos de filtro e contexto DAX.

Houve testes de modelo, cálculos e visuais, **mas não há registro de conclusão integral de todas as verificações planejadas**. Portanto, os totais consolidados, especialmente por grupo e serviço, **não devem ser considerados integralmente validados** apenas com base neste fechamento.

**Situação:** Fase 1 entregue e acesso à Fase 2 liberado. O encerramento administrativo não significa que a pendência técnica foi resolvida.
