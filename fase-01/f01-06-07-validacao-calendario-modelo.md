# F01-06 e F01-07 — Calendário e integridade do modelo

## Calendário

- `calendario[data]` confirmada como Data, com a tabela marcada como tabela de datas.
- `mes_ano` ordenado por `ano_mes` e `mes_nome` por `mes_numero`.
- Trocas de mês demonstraram o comportamento esperado nos filtros. Os testes em cartões foram registrados com valores arredondados.

## Integridade e filtros

Em **setembro/2026**, a tabela de teste por filial registrou **1.745 vendas distintas** e **R$ 9.760.630,53** em vendas líquidas.

| Teste | Resultado registrado |
|---|---|
| Vendas distintas na base completa | 45.000 de 45.000 |
| Vendas distintas em setembro/2026 | 1.745 de 1.745 |
| Itens sem venda; itens sem serviço; filiais sem cidade | 0 em cada verificação |
| Vendas sem filial | Nenhuma identificada |
| Chaves primárias das 11 tabelas | Únicas, sem nulos ou erros no perfilamento completo |

Os filtros por calendário, filial e cidade funcionaram nos testes; metas de valor e quantidade responderam aos filtros de mês e filial. Foram mantidos os **18 relacionamentos ativos e 4 inativos** definidos na F01-05. As medidas temporárias de teste não substituíram as medidas DAX definitivas.

**Limite do registro:** as verificações acima não significam que todos os indicadores e interações da entrega final foram integralmente aprovados. Ver [fechamento da fase](fechamento-fase-01.md).
