# Planejamento — Fase 2 | Squad 137

**Reunião:** 11/11/2026, à noite  
**Início:** 12/11/2026  
**Meta de entrega:** 22/11/2026, preferencialmente à tarde  
**Prazo oficial:** 23/11/2026, às 23h59 (Brasília)

O escopo e as fontes de dados estão no [README da Fase 2](README.md). A execução, as dependências de cada tarefa, os responsáveis, os revisores e os campos de acompanhamento ficam nas [Issues do Kanban](https://github.com/users/stephleao/projects/7/views/1), na milestone `Fase 2`. A `F02-23` foi incorporada à `F02-22` e encerrada; a [Issue #31](https://github.com/stephleao/educadados-aurora-squad137/issues/31) foi criada com a identificação `F02-23`; são **24 Issues ativas**.

## Cronograma

| Data | Entrega esperada | Issues |
|---|---|---|
| **11/11** | Reunião: distribuir tarefas, revisores e horários de edição | — |
| **12–13/11** | Importar `orcamentos`, ajustar modelo e validar medidas herdadas e filtros | `F02-01` a `F02-04`, `F02-23` |
| **14–17/11** | Criar e testar medidas de metas, orçamentos e participação | `F02-05` a `F02-11` |
| **18–20/11** | Concluir visuais, alertas e segmentações; cada integrante testa e integra sua contribuição | `F02-12` a `F02-18` |
| **21/11** | Integração coletiva, cinco perguntas, testes e correções | `F02-19` a `F02-21` |
| **22/11** | Publicar, testar links e enviar os dois links ao bootcamp | `F02-22` |
| **23/11** | Concluir a documentação técnica; prazo oficial e contingência para o painel | `F02-24` |

A `F02-19` envolve toda a squad na conferência da integração, e a `F02-21` envolve toda a squad nos testes finais. As demais tarefas seguem a regra de revisor independente do guia. Os visuais podem começar assim que suas medidas estiverem validadas. **Atenção ao dia 21:** testes e correções ocorrerão no mesmo dia; cada pessoa deve testar seu trabalho antes, para evitar descobertas tardias. A documentação (`F02-24`) deve ser atualizada progressivamente e pode ser finalizada até **23/11**. A parte necessária para enviar os links deve estar pronta na entrega de **22/11**.

## Regras técnicas que exigem atenção

- **Metas:** no nível de filial, meta de valor usa o nível Produto, e meta de quantidade usa o nível Vendedor. Não somar metas dos diferentes níveis (Produto, Serviço, Vendedor e Profissional).
- **Bases de cálculo:** vendas usam `vendas[valor_liquido]`; grupos e serviços usam o valor bruto de `itens_venda[valor_total]`. Quantidade de itens vem de `itens_venda[quantidade]`.
- **Atingimento:** aplicar as faixas sobre percentuais não arredondados: abaixo de 90%, de 90% até menos de 100% e 100% ou mais. Ausência de meta não equivale a 0%.
- **Orçamentos:** contar `orcamentos[codigo_orcamento]` pela data de criação. Conversão = orçamentos aprovados / gerados no período; taxa da rede = total de aprovados / total de gerados, e não média simples por filial.
- **Desconto e perdas:** calcular desconto de forma ponderada pelo valor bruto, validando quais `status` entram na regra. Valor líquido perdido é a soma de `orcamentos[valor_liquido]` com `orcamentos[status] = "Perdido"`.
- **Participação de serviços:** usar valores brutos de itens; a participação de cada serviço dentro do grupo deve somar 100% no contexto de filtros apropriado.
- **Filtros e metas ausentes:** conferir a interação de grupo de serviço que falhou na Fase 1 e manter visíveis as entidades sem metas cadastradas para 2026.

## Validação e entrega

O painel deve permitir responder, com o filtro **setembro/2026**:

1. Quantas filiais ativas atingiram a meta de valor, e quantas atingiram valor mas não quantidade?
2. Qual filial teve maior conversão de orçamentos e ela atingiu a meta de valor?
3. Qual valor líquido dos orçamentos perdidos e qual sua proporção sobre as vendas líquidas?
4. Quais filiais atingiram a meta de valor, mas ficaram abaixo da taxa de conversão da rede?
5. Qual a participação do grupo Alinhador no valor bruto da rede e qual serviço tem maior participação dentro dele?

A resposta deve ser obtida pelo próprio painel; um documento `.md` com respostas é opcional e interno.

## Lista de encerramento

- Conferir os requisitos, as segmentações e as cinco perguntas de setembro/2026.
- Realizar a conferência coletiva da integração (`F02-19`) e os testes finais com toda a squad (`F02-21`).
- Corrigir os problemas encontrados e repetir os testes necessários.
- Salvar `Aurora_squad_137_f02_final.pbix` em `Fase 2/02 Entrega` no Google Drive.
- Publicar no Power BI, testar os dois links sem login e guardar prints da publicação.
- Submeter os dois links ao bootcamp, preferencialmente em **22/11** (prazo oficial: **23/11 às 23h59**, Brasília).
- Finalizar a documentação técnica (`F02-24`) até **23/11**, sem bloquear a entrega do dia 22.

As regras de armazenamento, revisão independente e uso do GitHub estão no [guia de colaboração](../GUIA_COLABORACAO.md).
