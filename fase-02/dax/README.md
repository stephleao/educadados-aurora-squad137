# Medidas DAX — Fase 2

Esta pasta reúne as medidas criadas ou adaptadas para a Fase 2. Ao adicionar um arquivo `.dax`, indicar brevemente a finalidade da medida e os cuidados relevantes de cálculo ou filtro.

As medidas anteriores estão em [Fase 1 — DAX](../../fase-01/dax/README.md) e devem ser validadas no novo modelo antes do uso.

## Arquivos e tarefas

- [`participacao-grupos.dax`](participacao-grupos.dax): medidas de valor bruto total da rede e participação percentual dos grupos de serviço, desenvolvidas e testadas na F02-04.

- [`exibicao.dax`](exibicao.dax): medidas `Faixa Atingimento Valor` e `Faixa Atingimento Qtd`, desenvolvidas por Elide Paixão na F02-05. Classificam separadamente o atingimento de valor e quantidade, tratando metas ausentes como "Sem Meta".

- [`indicadores.dax`](indicadores.dax): oito medidas de contagem de filiais ativas por faixa de atingimento de valor e quantidade, desenvolvidas por Elide Paixão na F02-06. Utilizam `DISTINCTCOUNT` e `KEEPFILTERS`. Validação de setembro/2026: soma de 70 registros em cada conjunto de faixas.

- [`medidas-f02-07-08.dax`](medidas-f02-07-08.dax): oito medidas publicadas por Danielli Arçari em 16/11/2026.
  - **F02-07:** `Status Atingimento`, classificação das filiais segundo o atingimento das metas de valor e quantidade.
  - **F02-08:** `Orçamentos Gerados`, `Orçamentos Aprovados`, `Orçamentos Perdidos` e `Taxa de Conversão`.
  - **Relacionadas à F02-09:** `Desconto Médio Ponderado`, `Valor Líquido Orçamentos` e `Valor Perdido`, ainda sujeitas à conferência da implementação final da tarefa.

- [`medidas-f02-09.dax`](medidas-f02-09.dax): medidas complementares de desconto ponderado sobre orçamentos aprovados e percentual de valor perdido sobre vendas, relacionadas à F02-09 de Christian Farias. Reutiliza medidas já documentadas pela Dani. Testes de mês e filial realizados no Power BI.

- [`medidas-f02-10.dax`](medidas-f02-10.dax): medidas `Conversão da Rede` e `Diferença vs Rede`, relacionadas à F02-10 de Christian Farias. Calculam a referência agregada da rede e sua diferença em relação à filial. Testes realizados no Power BI.

## Validação das F02-07 e F02-08

- As quatro classificações de atingimento foram conferidas no Power BI, sem divergências observadas.
- Não foram encontradas filiais com metas em branco no contexto testado.
- As medidas de orçamentos responderam aos filtros de mês e filial.
- Os resultados das tabelas de conferência foram consistentes.
- A revisão independente pelo revisor indicado nas issues não foi confirmada neste registro.

## Referências

- [Issue #8 — F02-07](https://github.com/stephleao/educadados-aurora-squad137/issues/8)
- [Issue #9 — F02-08](https://github.com/stephleao/educadados-aurora-squad137/issues/9)
- [Issue #10 — F02-09](https://github.com/stephleao/educadados-aurora-squad137/issues/10)
- [Issue #11 — F02-10](https://github.com/stephleao/educadados-aurora-squad137/issues/11)
