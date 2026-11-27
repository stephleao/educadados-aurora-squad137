# Planejamento — Fase 3 | Squad 137

**Início:** 29/11/2026  
**Meta de desenvolvimento:** 03/12/2026  
**Meta de entrega:** 06/12/2026  
**Prazo oficial:** 07/12/2026, às 23h59 (Brasília)

O escopo e as fontes de dados estão no [README da Fase 3](README.md). A execução, as dependências, os responsáveis, os revisores e os campos de acompanhamento ficam nas [Issues do Kanban](https://github.com/users/stephleao/projects/7/views/1), na milestone `Fase 3`, com identificação `F03-*`.

A distribuição das tarefas será definida pela squad, considerando a disponibilidade dos integrantes e as dependências técnicas.

## Cronograma

| Data | Entrega esperada | Issues |
| --- | --- | --- |
| **29/11** | Alinhar responsabilidades, preparar o modelo, planejar o layout e iniciar os cálculos independentes | `F03-01`, `F03-02`, `F03-06`, `F03-07`, `F03-09` a `F03-12` |
| **30/11–02/12** | Desenvolver, testar e integrar as medidas DAX | `F03-03` a `F03-11` |
| **01–03/12** | Construir os visuais e integrar as contribuições conforme as dependências | `F03-13` a `F03-18` |
| **03/12** | Concluir o desenvolvimento, configurar segmentações e interações | `F03-19` |
| **04/12** | Conferência coletiva e validação das nove perguntas de aprovação | `F03-20`, `F03-21` |
| **05/12** | Corrigir divergências, repetir testes e aprovar a versão final | `F03-20`, `F03-21` |
| **06/12** | Publicar, testar os links e realizar a entrega oficial | `F03-22` |
| **07/12** | Contingência e prazo oficial | — |

A documentação (`F03-23`) deve ser atualizada progressivamente durante o desenvolvimento.

A Fase 3 parte do PBIX integrado e validado da Fase 2. A implementação do calendário por filial e das medidas de ritmo e projeção constitui a principal sequência de dependências. As demais frentes devem avançar em paralelo.

## Organização do painel

A Fase 3 acrescenta análises de:

- Ritmo mensal, acumulado, meta e projeção de fechamento por filial.
- Comparativos YoY, MoM e YTD e média móvel de três meses.
- Concentração das vendas por serviço, utilizando a curva ABC.
- Vendas por dia da semana e semana do mês.
- Desempenho e movimentação no ranking de vendedores.

A organização das páginas, dos filtros e da navegação será definida na `F03-12`, utilizando o [layout de referência no Figma](https://www.figma.com/design/LDOblJJ8KxFQ2SlVE4ycEh/Educadados---Aurora?node-id=22-7436).

As funcionalidades das fases anteriores devem ser preservadas.

## Regras técnicas que exigem atenção

- **Dias úteis:** calcular em medida por filial, considerando domingos, sábados úteis e feriados nacionais, estaduais e municipais. A coluna `calendario[dia_util]` não contempla todas essas particularidades.
- **Data de corte:** utilizar tabela desconectada, com simulação inicial em 20/09/2026, sem alterar o filtro de período da página.
- **Metas:** preservar as regras da Fase 1. A meta mensal integral não deve ser reduzida pela data de corte.
- **Projeção:** realizado até a data de corte ÷ dias úteis decorridos × dias úteis do mês, conforme o calendário da filial.
- **Comparativos temporais:** distinguir períodos completos e incompletos, tratar meses sem vendas e respeitar o limite da base, de 30/09/2026.
- **YoY:** apresentar rede total e mesmas filiais, considerando aquelas que já vendiam no mesmo mês do ano anterior.
- **Curva ABC:** utilizar o valor bruto de `itens_venda[valor_total]`, preservando os filtros de filial e período.
- **Vendedores:** distinguir meses com metas cadastradas, meses atingidos e ausência de histórico no ranking.
- **Modelagem:** avaliar o impacto dos novos relacionamentos e preservar as configurações anteriores quando não houver justificativa para alteração.

As convenções não especificadas pelo enunciado, como limites das classes ABC, tratamento de empates e definição de semana do mês, devem ser acordadas e registradas nas Issues correspondentes.

## Validação e entrega

O painel deve permitir responder às nove perguntas oficiais, respeitando os períodos e formatos definidos no desafio.

A conferência dos cálculos e dos requisitos deve ocorrer durante o desenvolvimento e ser consolidada na `F03-20` e na `F03-21`.

Utilizar o [checklist final de entrega](checklist-entrega.md) para acompanhar a validação dos requisitos e a publicação.

As regras de armazenamento, integração, revisão independente e uso do GitHub estão no [guia de colaboração](../GUIA_COLABORACAO.md).

**Prazo oficial:** 07/12/2026, às 23h59 (Brasília).
