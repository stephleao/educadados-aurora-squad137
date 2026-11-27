# Checklist final de entrega — Fase 3 | Squad 137

**Prazo oficial:** 07/12/2026, às 23h59 (Brasília).

Este checklist acompanha a conferência coletiva dos requisitos oficiais da Fase 3. Os detalhes de execução, dependências e revisão individual estão nas [Issues do Kanban](https://github.com/users/stephleao/projects/7/views/1).

Marcar os itens somente após a validação correspondente.

## 1. Dados e modelagem

- [ ] PBIX de partida da Fase 2 identificado e validado.
- [ ] Tabela `feriados` importada e conferida conforme o dicionário.
- [ ] Relacionamentos e tipos de dados validados.
- [ ] Medidas herdadas necessárias à fase conferidas.

## 2. O que a tela precisa ter

- [ ] Seletor de data de corte.
- [ ] Acumulado × meta.
- [ ] Projeção de fechamento por filial usando os dias úteis da própria filial.
- [ ] YoY, MoM e YTD.
- [ ] Média móvel de 3 meses.
- [ ] Curva ABC de serviços.
- [ ] Vendas por dia da semana.
- [ ] Ranking de vendedores com variação de posição.
- [ ] Tratamento de filiais novas.

## 3. Desafios de DAX

- [ ] Vendedores que bateram a meta em todos os meses do ano: medida que conta os meses batidos e compara com os meses com meta.
- [ ] Dias úteis por filial calculados em medida, cruzando calendário, feriados (nacional, estadual e municipal) e o sábado útil de cada filial, sem coluna fixa de dia útil por filial.
- [ ] Data de corte em tabela desconectada: todas as medidas de acumulado, ritmo e projeção respondem ao seletor, sem alterar o filtro de período da página.
- [ ] YoY em duas versões: total da rede e "mesmas filiais" (só as que já vendiam no mesmo mês do ano anterior), com a diferença entre as duas explicada na tela.
- [ ] YTD, MoM e média móvel de 3 meses com funções de inteligência de tempo, tratando meses sem venda e o mês incompleto.
- [ ] Curva ABC com ranking e percentual acumulado feitos em medida, de modo que as classes A, B e C mudem conforme o filtro de filial e de período.
- [ ] Variação de posição no ranking de vendedores: posição do mês, posição do mês anterior e quantas posições subiu ou desceu.
- [ ] Ritmo necessário: quanto a filial precisa vender por dia útil restante para fechar o mês na meta.

## 4. Desafios de visual

- [ ] Gráfico de ritmo do mês: acumulado diário realizado, linha da meta distribuída pelos dias úteis e projeção até o último dia.
- [ ] Pareto da curva ABC: colunas por serviço, linha do percentual acumulado e a marca dos 80%.
- [ ] Mapa de calor de vendas por dia da semana e semana do mês, com formatação condicional.
- [ ] Pequenos múltiplos por regional comparando o ano atual com o anterior.
- [ ] Ranking de vendedores com setas e cores de subida e queda de posição.
- [ ] Tooltip de página por filial com dias úteis do mês, dias decorridos, projeção e ritmo necessário.
- [ ] Filiais novas sinalizadas na tela (sem base de comparação), em vez de aparecerem com crescimento infinito ou em branco.

## 5. Perguntas de aprovação

- [ ] P1 — Quantos vendedores bateram a meta de valor em todos os meses de janeiro a setembro de 2026?
- [ ] P2 — Quantos dias úteis teve setembro/2026 para a filial 1 e para a filial 4, segundo o calendário de cada uma?
- [ ] P3 — Com 'hoje' em 20/09/2026, qual a projeção de fechamento de setembro/2026 em valor líquido da filial 1 e ela fecha acima ou abaixo da meta?
- [ ] P4 — Qual a variação percentual do valor líquido da rede em setembro/2026 contra setembro/2025 (YoY) e contra agosto/2026 (MoM)?
- [ ] P5 — Em quais meses de 2025 a rede ficou abaixo da meta total de valor?
- [ ] P6 — Entre as filiais que já vendiam em setembro/2025, qual teve o maior crescimento percentual YoY em setembro/2026?
- [ ] P7 — Qual foi o valor líquido acumulado da rede de janeiro a setembro de 2026 e a variação percentual contra o mesmo período de 2025?
- [ ] P8 — Em 2025, quantos serviços respondem por 80% do valor total vendido da rede, ordenando do maior para o menor?
- [ ] P9 — Qual a média móvel de 3 meses (julho, agosto e setembro/2026) do valor líquido vendido pela rede?

Conferir os formatos de resposta e as regras de cálculo indicados no enunciado oficial.

## 6. Testes de regressão e usabilidade

- [ ] Datas de corte e filtros de período testados.
- [ ] Filiais com calendários distintos conferidas.
- [ ] Casos sem meta, sem venda e sem histórico tratados.
- [ ] Filtros, interações, tooltip e navegação testados.
- [ ] Funcionalidades das fases anteriores preservadas.
- [ ] Revisões independentes concluídas.
- [ ] Versão integrada aprovada pela squad.

## 7. Publicação e entrega

- [ ] Arquivo `Aurora_squad_137_f03_final.pbix` salvo na pasta `Fase 3/02 Entrega`.
- [ ] Painel publicado na web.
- [ ] PBIX compartilhado para qualquer pessoa com o link.
- [ ] Ambos os links testados em janela anônima, sem solicitar login.
- [ ] Entrega submetida na plataforma dentro do prazo.
- [ ] Confirmação e links registrados em `entregas/fase-03.md`.

## 8. Documentação técnica

- [ ] Alterações do modelo documentadas.
- [ ] Medidas DAX e respectivos testes registrados.
- [ ] Limitações técnicas identificadas documentadas.
- [ ] Índices e links atualizados.

A documentação deve refletir o trabalho efetivamente implementado e validado.
