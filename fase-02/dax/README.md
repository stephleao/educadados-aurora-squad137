# Medidas DAX — Fase 2

Esta pasta reúne as medidas criadas ou adaptadas para a Fase 2. Ao adicionar um arquivo `.dax`, indicar brevemente a finalidade da medida e os cuidados relevantes de cálculo ou filtro.

As medidas anteriores estão em [Fase 1 — DAX](../../fase-01/dax/README.md) e devem ser validadas no novo modelo antes do uso.

- [`participacao-grupos.dax`](participacao-grupos.dax): medidas de valor bruto total da rede e participação percentual dos grupos de serviço, desenvolvidas e testadas na `F02-04`.
- [`exibicao.dax`](exibicao.dax): medidas `Faixa Atingimento Valor` e `Faixa Atingimento Qtd`, desenvolvidas por Elide Paixão na F02-05. Classificam o atingimento de valor e quantidade separadamente nas faixas abaixo de 90%, de 90% a menos de 100% e 100% ou mais, tratando metas ausentes como "Sem Meta".

- [`indicadores.dax`](indicadores.dax): oito medidas de contagem de filiais ativas por faixa de atingimento de valor e quantidade, desenvolvidas por Elide Paixão na F02-06. Utilizam `DISTINCTCOUNT` e `KEEPFILTERS` para respeitar os filtros. Validação realizada em setembro/2026, com soma de 70 registros em cada conjunto de faixas.
