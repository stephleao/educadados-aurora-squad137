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

**Limitação técnica conhecida:** ao selecionar uma categoria do gráfico de grupos de serviço, o indicador percentual não atualizava conforme solicitado. A causa não foi confirmada. Ver [fechamento da Fase 1](fase-01/fechamento-fase-01.md).

### Fase 2 — Atingimento, orçamentos e composição das vendas

**Situação:** em desenvolvimento · **Entrega planejada:** 22/11/2026 · **Prazo oficial:** 23/11/2026, às 23h59 (Brasília).

Continuidade do painel comercial, com metas separadas de valor e quantidade, análise de orçamentos e participação dos grupos e serviços.

[Escopo, fontes e documentos da Fase 2](fase-02/README.md) · [Planejamento](fase-02/planejamento-fase-02.md)

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

**Guia de colaboração:** consulte [`GUIA_COLABORACAO.md`](GUIA_COLABORACAO.md) para regras de nomenclatura, versões de `.pbix` no Drive, integração individual e revisão via Pull Request.

## Organização dos arquivos

### GitHub

O repositório organiza a documentação e as medidas DAX separadamente por fase:

- [`fase-01/`](fase-01/README.md) — arquivos e medidas da Fase 1, preservados como histórico.
- [`fase-02/`](fase-02/README.md) — documentos e DAX da Fase 2.
- [`entregas/`](entregas/fase-01.md) — checklists, links e evidências de cada entrega.

As fases seguintes devem seguir o mesmo padrão. Os documentos anteriores não são reescritos como se fossem entregas da equipe atual.

### Google Drive

Os arquivos PBIX, as planilhas e os recursos visuais ficam na [pasta compartilhada da Squad 137](https://drive.google.com/drive/u/0/folders/1VJa4noEcfs4FtKLIBLxVfTSwJWF7dzUr):

```text
Fase 1/
├── 01 WIP/
└── 02 Entrega/
Fase 2/
├── 01 WIP/
└── 02 Entrega/
Logomarca/
Base de dados/
```

- **01 WIP:** versões em desenvolvimento.
- **02 Entrega:** arquivos finais apresentados ao bootcamp.
- **Logomarca:** materiais de identidade visual.
- **Base de dados:** planilhas originais e dados do desafio.

O GitHub guarda documentação, DAX e histórico de alterações; o Drive guarda os arquivos de trabalho e de entrega do Power BI.

## Documentação e entregas

- [Índice da Fase 1](fase-01/README.md)
- [Índice da Fase 2](fase-02/README.md)

### Fase 1 — histórico

- [Regras de negócio](fase-01/regras-de-negocio.md)
- [Modelo de dados](fase-01/modelo-de-dados.md)
- [Medidas DAX](fase-01/dax/README.md)
- [Fechamento da Fase 1](fase-01/fechamento-fase-01.md)
- [Tarefas da Fase 1](fase-01/tarefas-desafio-fase-01.md)
- [Checklist e links da entrega da Fase 1](entregas/fase-01.md)
- [Pasta da entrega da Fase 1](https://drive.google.com/drive/u/0/folders/1krieeIuUMqU_8z_QgoRmN4yuQf-jqyRC)

### Fase 2 — fontes do desafio

- **Enunciado:** [Desafio Fase 2](https://aulas.educadados.com.br/bootcamp/fases/2).
- **Referência de estrutura e relacionamentos:** `00_dicionario_de_dados.xlsx`.
- [Pasta oficial de dados do desafio](https://drive.google.com/drive/folders/1r67J4QuS4i4EjbVqPbyy0Vq4AzsKZgd8)
- [Manual visual da Rede Aurora no Figma](https://www.figma.com/design/RlCb3g2x0Ul6qalctSH0HV/Rede-Aurora-Odontologia-%E2%80%94-Logo?node-id=0-1&p=f)

Os documentos específicos de execução da Fase 2 serão adicionados conforme o andamento da equipe.

## Origem e histórico

Este repositório foi duplicado a partir de [educadados-aurora-painel](https://github.com/stephleao/educadados-aurora-painel), utilizado durante a Fase 1.

A implementação inicial foi desenvolvida antes da formação da Squad 137. A utilização desse trabalho pela equipe atual ocorreu com autorização de Stephanne Leão e do bootcamp. O histórico original de commits foi mantido para preservar a rastreabilidade das contribuições.
