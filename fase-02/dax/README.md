# Medidas DAX — Fase 2

Esta pasta reúne as medidas criadas ou adaptadas para a Fase 2. Ao adicionar um arquivo `.dax`, indicar brevemente a finalidade da medida e os cuidados relevantes de cálculo ou filtro.

As medidas anteriores estão em [Fase 1 — DAX](../../fase-01/dax/README.md) e devem ser validadas no novo modelo antes do uso.

## Arquivos e tarefas

- [`participacao-grupos.dax`](participacao-grupos.dax):
  - **F02-04:** medidas `Valor Bruto Total Rede` e `% Participação Grupo Rede`, desenvolvidas por Steph. Calculam o valor bruto total da rede e a participação dos grupos de serviço.
  - **F02-11:** medida `% Participação Serviço Grupo`, desenvolvida por Steph. Calcula a participação de cada serviço dentro do próprio grupo, preservando o contexto de grupo e utilizando valores brutos.
  - **Validação F02-11:** os serviços de Protocolo e Ortodontia (Aparelho Fixo) totalizaram 100% em setembro/2026. Os filtros de período e filial foram testados. Revisão independente pendente.

- [`exibicao.dax`](exibicao.dax): medidas `Faixa Atingimento Valor` e `Faixa Atingimento Qtd`, desenvolvidas por Elide Paixão na F02-05. Classificam separadamente o atingimento de valor e quantidade, tratando metas ausentes como "Sem Meta".

- [`indicadores.dax`](indicadores.dax): oito medidas de contagem de filiais ativas por faixa de atingimento de valor e quantidade, desenvolvidas por Elide Paixão na F02-06. Utilizam `DISTINCTCOUNT` e `KEEPFILTERS`. Validação de setembro/2026: soma de 70 registros em cada conjunto de faixas.

**Integração F02-12 e F02-13:** rótulo da faixa intermediária padronizado para "90% a 99%", preservando os limites numéricos e atualizando as comparações das medidas de contagem.

- [`medidas-f02-07-08.dax`](medidas-f02-07-08.dax): oito medidas publicadas por Danielli Arçari em 16/11/2026.
  - **F02-07:** `Status Atingimento`, classificação das filiais segundo o atingimento das metas de valor e quantidade.
  - **F02-08:** `Orçamentos Gerados`, `Orçamentos Aprovados`, `Orçamentos Perdidos` e `Taxa de Conversão`.
  - **Relacionadas à F02-09:** `Desconto Médio Ponderado`, `Valor Líquido Orçamentos` e `Valor Perdido`, ainda sujeitas à conferência da implementação final da tarefa.

- [`medidas-f02-09.dax`](medidas-f02-09.dax): medidas complementares de desconto ponderado sobre orçamentos aprovados e percentual de valor perdido sobre vendas, relacionadas à F02-09 de Christian Farias. Reutiliza medidas já documentadas pela Dani. Testes de mês e filial realizados no Power BI.

- [`medidas-f02-10.dax`](medidas-f02-10.dax): medidas `Conversão da Rede` e `Diferença vs Rede`, relacionadas à F02-10 de Christian Farias. Calculam a referência agregada da rede e sua diferença em relação à filial. Testes realizados no Power BI.

- [`medidas-f02-12.dax`](medidas-f02-12.dax):
  - **F02-12:** tabela auxiliar `Filtro Situacao Atingimento` e medida `Exibir Filial Ating`, desenvolvidas por Steph.
  - Permitem filtrar dinamicamente a matriz de atingimento das filiais conforme a situação selecionada, reutilizando a medida `Status Atingimento` da F02-07.
  - Inclui a configuração da matriz e a formatação condicional dos percentuais.
  - **Validação:** testadas todas as opções do filtro de situação e as segmentações de período e filial. Conferida a coerência dos percentuais, classificações e totais no cenário de Somente Valor.
  - **Ressalva técnica:** o tratamento de ausência parcial de metas e de metas iguais a zero permanece como ponto de revisão futura. Essa ressalva não altera a regra anual de ausência de cadastro de metas da F02-17.

- [`medidas-f02-13.dax`](medidas-f02-13.dax):
  - **F02-13:** tabela auxiliar `dFaixas` e quatro medidas de indicadores, desenvolvidas por Danielli Arçari.
  - Apresentam as contagens de filiais por faixa de atingimento de valor e quantidade, além das contagens de filiais que atingiram somente uma das metas.
  - **Integração:** realizada por Steph, reunindo os indicadores da F02-13 e a matriz da F02-12 no mesmo PBIX, com padronização dos rótulos das faixas e inclusão de `KEEPFILTERS` nas medidas de atingimento exclusivo para restringir as contagens às filiais ativas.
  - **Validação:** em setembro/2026, os gráficos totalizaram 70 filiais cada. Foram observadas 40 filiais com meta de valor atingida e 46 com meta de quantidade atingida. Os cartões apresentaram 6 filiais com atingimento exclusivo de valor e 12 com atingimento exclusivo de quantidade.
  - **Ressalva técnica:** o tratamento de ausência parcial de metas e de metas iguais a zero permanece como ponto de revisão futura, conforme documentação da F02-12.

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
- [Issue #13 — F02-12](https://github.com/stephleao/educadados-aurora-squad137/issues/13)
- [Issue #14 — F02-13](https://github.com/stephleao/educadados-aurora-squad137/issues/14)
