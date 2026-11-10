# Planejamento da Fase 2 — Painel Aurora | Squad 137

**Repositório:** `stephleao/educadados-aurora-squad137`  
**Kanban:** [Painel Aurora - Squad 137](https://github.com/users/stephleao/projects/7/views/1)  
**Milestone:** `Fase 2` (vinculação às Issues a conferir)  
**Reunião:** 11/11/2026, à noite  
**Início do desenvolvimento:** 12/11/2026  
**Entrega oficial:** **23/11/2026, às 23h59 (Brasília)**

## 1. Objetivo

Evoluir o relatório da Fase 1 com atingimento separado de metas de valor e quantidade, três faixas de atingimento, filiais que atingiram apenas uma das metas, funil de orçamentos, conversão por filial e média da rede, desconto médio ponderado, valor perdido, matriz hierárquica grupo de serviço > serviço, participações percentuais, segmentações e alerta de metas ausentes em 2026.

A Fase 2 reutiliza os 11 arquivos da Fase 1 e acrescenta `orcamentos.xlsx`. Outras tabelas do catálogo geral não são obrigatórias pelo enunciado específico desta fase.

## 2. Princípios

- Atribuições individuais serão definidas na reunião de 11/11, considerando dificuldade, esforço e disponibilidade. Nenhuma Issue terá responsável antes disso.
- Reaproveitar os campos existentes do Project. Usar a milestone `Fase 2`; não criar label redundante `fase-02`.
- Cada Issue tem checklist, dependências e critério de conclusão. Conferir no `.pbix`, DAX ou Drive, sem prints obrigatórios de rotina.
- Preservar a Fase 1 e examinar impactos antes de modificar o modelo.
- Medidas numéricas permanecem numéricas; textos de apresentação como `"sem meta"` são separados quando necessário.
- Alterações de código e documentação utilizam branch própria, PR e revisão antes do merge em `main`.
- O `.pbix` e as planilhas ficam no Google Drive, **não no GitHub**.

## 3. Cuidados técnicos

1. **Metas:** para filial, valor usa nível Produto e quantidade usa nível Vendedor. Os quatro níveis Produto, Serviço, Vendedor e Profissional são independentes e não devem ser somados entre si.
2. **Realizado:** vendas usam `vendas[valor_liquido]` e contagem de vendas; grupo/serviço usam `itens_venda[valor_total]` e soma de `itens_venda[quantidade]`.
3. **Faixas:** usar percentual numérico não arredondado: abaixo de 90%, de 90% até menos de 100%, e 100% ou mais; ausência de meta é um caso separado.
4. **Orçamentos:** contar `orcamentos[codigo_orcamento]` pela data de criação. Conversão = aprovados / criados. Taxa da rede = total aprovado / total criado, nunca média simples das taxas das filiais.
5. **Desconto:** utilizar ponderação pelo valor bruto, conferindo os status elegíveis antes de homologar.
6. **Perdas:** valor líquido perdido = soma de `orcamentos[valor_liquido]` para `orcamentos[status] = "Perdido"`.
7. **Serviços:** participação usa o valor bruto `itens_venda[valor_total]`; os serviços precisam somar 100% dentro do grupo no contexto de filtros pertinente.
8. **Pendência da Fase 1:** investigar a seleção do gráfico de grupos que não atualizava o percentual, avaliando DAX, interações e caminhos de filtro.
9. **Meta ausente:** verificar falta de cadastro de meta em 2026 sem ocultar entidades e sem transformar ausência em 0%.

## 4. Backlog das Issues

| Código | Issue | Pontos | Dependências |
|---|---|---:|---|
| `F02-01` | [Importar e tratar `orcamentos`](https://github.com/stephleao/educadados-aurora-squad137/issues/2) | 3 | — |
| `F02-02` | [Modelar e validar relacionamentos](https://github.com/stephleao/educadados-aurora-squad137/issues/3) | 3 | F02-01 |
| `F02-03` | [Validar medidas herdadas](https://github.com/stephleao/educadados-aurora-squad137/issues/4) | 3 | — |
| `F02-04` | [Investigar filtro por grupo](https://github.com/stephleao/educadados-aurora-squad137/issues/5) | 3 | F02-03 |
| `F02-05` | [Faixas de atingimento](https://github.com/stephleao/educadados-aurora-squad137/issues/6) | 3 | F02-03 |
| `F02-06` | [Contagem por faixas](https://github.com/stephleao/educadados-aurora-squad137/issues/7) | 3 | F02-05 |
| `F02-07` | [Filiais com apenas uma meta atingida](https://github.com/stephleao/educadados-aurora-squad137/issues/8) | 2 | F02-05 |
| `F02-08` | [Volume e conversão de orçamentos](https://github.com/stephleao/educadados-aurora-squad137/issues/9) | 3 | F02-02 |
| `F02-09` | [Desconto ponderado e valor perdido](https://github.com/stephleao/educadados-aurora-squad137/issues/10) | 3 | F02-02 |
| `F02-10` | [Conversão agregada da rede](https://github.com/stephleao/educadados-aurora-squad137/issues/11) | 3 | F02-08 |
| `F02-11` | [Participação da rede e dentro do grupo](https://github.com/stephleao/educadados-aurora-squad137/issues/12) | 4 | F02-03, F02-04 |
| `F02-12` | [Matriz de atingimento](https://github.com/stephleao/educadados-aurora-squad137/issues/13) | 3 | F02-05, F02-07 |
| `F02-13` | [Cartões de atingimento](https://github.com/stephleao/educadados-aurora-squad137/issues/14) | 2 | F02-06 |
| `F02-14` | [Funil de orçamentos](https://github.com/stephleao/educadados-aurora-squad137/issues/15) | 2 | F02-08 |
| `F02-15` | [Conversão por filial](https://github.com/stephleao/educadados-aurora-squad137/issues/16) | 2 | F02-10 |
| `F02-16` | [Matriz grupo > serviço](https://github.com/stephleao/educadados-aurora-squad137/issues/17) | 3 | F02-11 |
| `F02-17` | [Página de alerta sem meta](https://github.com/stephleao/educadados-aurora-squad137/issues/18) | 3 | F02-03 |
| `F02-18` | [Segmentações e interações](https://github.com/stephleao/educadados-aurora-squad137/issues/19) | 2 | F02-12, F02-14, F02-16, F02-17 |
| `F02-19` | [Conferência coletiva da integração final](https://github.com/stephleao/educadados-aurora-squad137/issues/20) | 2 | F02-12 a F02-18 |
| `F02-20` | [Validar as cinco perguntas no painel](https://github.com/stephleao/educadados-aurora-squad137/issues/21) | 3 | F02-07 a F02-11, F02-19 |
| `F02-21` | [Testes finais](https://github.com/stephleao/educadados-aurora-squad137/issues/22) | 2 | F02-18 a F02-20 |
| `F02-22` | [Publicação e entrega oficial](https://github.com/stephleao/educadados-aurora-squad137/issues/23) | Consultar Project | F02-19, F02-20, F02-21, F02-24 |
| `F02-23` | [Incorporada à F02-22; Issue encerrada](https://github.com/stephleao/educadados-aurora-squad137/issues/24) | — | — |
| `F02-24` | [Documentação técnica](https://github.com/stephleao/educadados-aurora-squad137/issues/25) | 2 | F02-19, F02-20 |

**Total:** 23 Issues ativas; a `F02-23` foi incorporada à `F02-22` e encerrada para preservar o histórico. O esforço atual deve ser consultado nos campos do GitHub Project, inclusive após os ajustes da equipe. Os detalhes e checklists estão nos corpos das Issues. Responsáveis permanecem indefinidos.

## 5. Cronograma

**Meta interna de entrega:** **22/11/2026 (domingo)**, preferencialmente durante a tarde.  
**Prazo oficial:** **23/11/2026, às 23h59 (Brasília)**; o dia 23 fica reservado para contingências.

| Data | Atividades | Issues |
|---|---|---|
| 11/11 (quarta), à noite | Reunião para definir responsáveis, esforço e horários de integração | — |
| 12–13/11 (quinta–sexta) | Importação de `orcamentos`, modelo, revisão de medidas herdadas e investigação dos filtros | `F02-01` a `F02-04` |
| 14–17/11 (sábado–terça) | Medidas DAX de atingimento, faixas, conversão, desconto, valor perdido e participação, em frentes paralelas | `F02-05` a `F02-11` |
| 18–20/11 (quarta–sexta) | Construir e finalizar matrizes, cartões, funil, gráfico, alerta e segmentações; cada integrante testa e integra sua própria contribuição durante o desenvolvimento | `F02-12` a `F02-18` |
| 21/11 (sábado) | Fazer a integração final e conferência coletiva do `.pbix`; validar as cinco perguntas de setembro/2026, executar testes gerais, corrigir defeitos e repetir os testes necessários | `F02-19`, `F02-20` e `F02-21` |
| 22/11 (domingo) | Publicar o relatório, salvar o `.pbix` final no Google Drive, testar ambos os links em janela anônima e realizar a entrega oficial | `F02-22` |
| 23/11 (segunda) | Prazo oficial; usar apenas como contingência se houver impedimentos no dia 22 | — |

A `F02-24` (documentação técnica) será realizada progressivamente e finalizada até **21/11**.

**Marcos de conclusão sugeridos:**

- **13/11:** `F02-01` a `F02-04` — 4 Issues concluídas acumuladas.
- **17/11:** `F02-05` a `F02-11` — 11 Issues concluídas acumuladas.
- **20/11:** `F02-12` a `F02-18` — 18 Issues concluídas acumuladas.
- **21/11:** `F02-19`, `F02-20`, `F02-21` e `F02-24` — 22 Issues concluídas acumuladas.
- **22/11:** `F02-22` — 23 Issues ativas concluídas acumuladas; `F02-23` permanece encerrada como incorporada.

Os campos de esforço do Project representam esforço relativo, não horas, e são a fonte atualizada após os ajustes da equipe. Os integrantes podem antecipar visuais assim que suas medidas forem validadas, sem esperar o início formal da etapa seguinte.

**Risco do cronograma:** a conferência da integração final, a validação e as correções compartilham o dia 21. Por isso, cada integrante deve integrar e testar suas medidas e visuais durante o desenvolvimento; no sábado, a equipe revisa o conjunto e resolve inconsistências. Problemas grandes descobertos no fim podem exigir a contingência de 23/11.

**Dependências que podem atrasar a entrega:**

- `F02-01` → `F02-02` → `F02-08` → `F02-10` → `F02-15` → `F02-18` → `F02-19` → `F02-20` → `F02-21` → `F02-22`.
- `F02-03` → `F02-04` → `F02-11` → `F02-16` → `F02-18`.

Essas sequências indicam bloqueios possíveis, não um caminho crítico calculado em horas.

## 6. Integração e arquivos da Fase 2

As regras permanentes estão em [`GUIA_COLABORACAO.md`](../GUIA_COLABORACAO.md). No Google Drive, usar `Fase 2/01 WIP` para desenvolvimento e `Fase 2/02 Entrega` para entrega.

- Cada pessoa desenvolve, testa **e integra a própria contribuição** no `.pbix` de trabalho.
- Uma pessoa por vez edita o arquivo principal; antes de trabalhar, confirma a versão atual e reserva o período de edição com a equipe.
- Salvar o trabalho em `01 WIP` seguindo `Aurora_[TAREFA]_[RESPONSÁVEL].pbix`, acrescentando `_wip` ou `_incompleto` quando pertinente.
- Não descartar versão anterior sem confirmar que suas alterações já estão integradas.
- A `F02-19` é uma **conferência coletiva** do resultado, não uma centralização da integração.
- O arquivo final vai para `02 Entrega` como `Aurora_squad_137_f02_final.pbix`, com prints de publicação.
- A entrega oficial é o link público do Power BI e o link do `.pbix` no Google Drive, testados sem login.

## 7. Perguntas de aprovação

Para setembro/2026, o painel deve permitir responder:

1. Quantas filiais ativas bateram 100% da meta de valor; quantas bateram valor, mas não quantidade.
2. Qual filial teve a maior conversão e se bateu a meta de valor.
3. Qual o valor líquido perdido e sua proporção sobre o valor líquido vendido.
4. Quais filiais bateram a meta de valor com conversão inferior à taxa agregada da rede.
5. Qual a participação do grupo Alinhador na rede e qual serviço lidera sua participação interna.

Um documento `.md` de respostas é **opcional, apenas para uso da equipe**, e não é parte da entrega oficial.

## 8. Checklist final

- [ ] Metas de valor e quantidade, faixas e filiais que atingiram somente uma meta validadas.
- [ ] Funil, taxa agregada de conversão, desconto ponderado e valor perdido corretos.
- [ ] Matriz grupo > serviço mostra participação na rede e soma 100% por grupo.
- [ ] Página de alerta mostra entidades sem meta cadastrada para 2026.
- [ ] Segmentações de ano, mês e filial funcionam.
- [ ] O painel permite responder às cinco perguntas de setembro/2026.
- [ ] Regressões da Fase 1 e pendência de filtro verificadas.
- [ ] `.pbix` final está no Google Drive, com link testado sem login.
- [ ] Relatório publicado na web, com link testado sem login.
- [ ] Prints da publicação salvos em `02 Entrega`.
- [ ] Dois links enviados até 23/11/2026, às 23h59 (Brasília).

## 9. Próximos passos

1. Vincular as Issues à milestone `Fase 2` e ao Project nº 7, conferindo campos existentes.
2. Na reunião de 11/11, definir responsáveis, esforço e janelas exclusivas de edição.
3. Iniciar a execução em 12/11.
