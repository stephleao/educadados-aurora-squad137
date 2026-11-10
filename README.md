# Painel Aurora — Squad 137 | Bootcamp Educadados

Projeto de análise de dados do Bootcamp Educadados, utilizando o cenário da Rede Aurora Odontologia.

Este repositório é a continuidade do projeto pela **Squad 137**, preservando os arquivos e o histórico de commits da Fase 1.

## Sobre o projeto

O Painel Aurora transforma dados comerciais e operacionais em indicadores para análise e tomada de decisão no Power BI.

### Fase 1 — Comercial

**Histórico de entregas:**
- **07/11/2026:** entrega realizada por Stephanne Leão na squad anterior.
- **09/11/2026:** entrega realizada pela Squad 137, com autorização para utilizar o trabalho desenvolvido anteriormente.

A Fase 1 inclui um relatório comercial com até duas páginas, contendo:
- Vendas em valor e quantidade, metas e percentuais de atingimento;
- Análises por rede, filial, cidade, vendedor, profissional, grupo de serviço e serviço;
- Gráficos, matrizes, filtros por período, rótulos combinados e formatação condicional;
- Indicação de "sem meta" na tabela de serviços.

**Limitação técnica conhecida:** ao selecionar uma categoria do gráfico de grupos de serviço, o indicador percentual não atualizava conforme solicitado. A causa não foi confirmada. Ver [fechamento da Fase 1](docs/fechamento-fase-01.md).

### Fase 2 — Atingimento, orçamentos e composição das vendas

**Período:** 08/11/2026 a 23/11/2026  
**Prazo de entrega:** 23/11/2026 às 23h59 (Brasília)  
**Situação:** em desenvolvimento pela Squad 137.

Conforme o enunciado da Fase 2, o relatório deve incorporar:
- Atingimento de metas de **valor e quantidade separadamente**, com faixas abaixo de 90%, de 90% a 99% e de 100% ou mais;
- Filiais que atingiram apenas uma das duas metas;
- Funil de orçamentos (gerados, aprovados e perdidos), taxa de conversão por filial, desconto médio ponderado e valor perdido;
- Matriz hierárquica **grupo de serviço > serviço**, com participação no total da rede e dentro do grupo;
- Segmentações por ano, mês e filial;
- Página de alerta para ausência de metas cadastradas em 2026.

A base da Fase 2 reutiliza os 11 arquivos da Fase 1 e acrescenta `orcamentos.xlsx`. As validações e medidas novas devem seguir o dicionário de dados e o enunciado da Fase 2.

## Equipe — Squad 137

| Integrante | GitHub | LinkedIn |
|---|---|---|
| Stephanne Leão | [@stephleao](https://github.com/stephleao) | [LinkedIn](https://www.linkedin.com/in/stephanne-leao) |
| Christian Farias | [@Christian-Farias](https://github.com/Christian-Farias) | [LinkedIn](https://www.linkedin.com/in/christian-farias-oliveira) |
| Elide Paixão | [@elidepaixao](https://github.com/elidepaixao) | [LinkedIn](https://www.linkedin.com/in/elidepaixao) |
| Danielli Arçari | [@danielli-arcari](https://github.com/danielli-arcari) | [LinkedIn](https://www.linkedin.com/in/danielli-arcari) |

As responsabilidades da Fase 2 serão organizadas pela equipe.

## Gestão e colaboração

- [Kanban — Painel Aurora - Squad 137](https://github.com/users/stephleao/projects/7/views/1)
- [Issues do repositório da Squad 137](https://github.com/stephleao/educadados-aurora-squad137/issues)
- [Pasta de trabalho da Squad 137 no Google Drive](https://drive.google.com/drive/u/0/folders/1VJa4noEcfs4FtKLIBLxVfTSwJWF7dzUr)

Fluxo de trabalho sugerido: **Backlog → A fazer → Em andamento → Em revisão → Concluído**.

Evitar a edição simultânea do mesmo arquivo PBIX. Arquivos de dados e relatórios Power BI são compartilhados em armazenamento externo, conforme as permissões definidas pela equipe.

## Organização do repositório

| Local | Conteúdo |
|---|---|
| `dax/` | Medidas DAX e documentação dos cálculos |
| `docs/` | Regras de negócio, modelo, planejamento e registros técnicos |
| `entrega/` | Checklists e links das entregas |

## Documentação e entregas

### Fase 1 — histórico

- [Regras de negócio](docs/regras-de-negocio.md)
- [Modelo de dados](docs/modelo-de-dados.md)
- [Medidas DAX](dax/README.md)
- [Fechamento da Fase 1](docs/fechamento-fase-01.md)
- [Tarefas da Fase 1](docs/tarefas-desafio-fase-01.md)
- [Checklist e links da entrega da Fase 1](entrega/README.md)
- [Pasta da entrega da Fase 1](https://drive.google.com/drive/u/0/folders/1krieeIuUMqU_8z_QgoRmN4yuQf-jqyRC)

### Fase 2 — fontes do desafio

- **Enunciado:** `Desafio_Fase_2.md` (fonte disponibilizada no projeto de estudos).
- **Referência de estrutura e relacionamentos:** `00_dicionario_de_dados.xlsx`.
- [Pasta oficial de dados do desafio](https://drive.google.com/drive/folders/1r67J4QuS4i4EjbVqPbyy0Vq4AzsKZgd8)
- [Manual visual da Rede Aurora no Figma](https://www.figma.com/design/RlCb3g2x0Ul6qalctSH0HV/Rede-Aurora-Odontologia-%E2%80%94-Logo?node-id=0-1&p=f)

Os documentos específicos de execução da Fase 2 serão adicionados conforme o andamento da equipe.

## Origem e histórico

Este repositório foi duplicado a partir de [educadados-aurora-painel](https://github.com/stephleao/educadados-aurora-painel), utilizado durante a Fase 1.

A implementação inicial foi desenvolvida antes da formação da Squad 137. A utilização desse trabalho pela equipe atual ocorreu com autorização de Stephanne Leão e do bootcamp. O histórico original de commits foi mantido para preservar a rastreabilidade das contribuições.
