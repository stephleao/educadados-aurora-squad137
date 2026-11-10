# Modelo de dados — Fase 1

O modelo usa **11 tabelas**: quatro fatos (`vendas`, `itens_venda`, `metas_valor`, `metas_quantidade`) e sete dimensões (`calendario`, `cidades`, `filiais`, `profissionais`, `vendedores`, `grupos_servico`, `servicos`).

Foram configurados os **22 relacionamentos** previstos no dicionário, com cardinalidade `*:1` e direção de filtro única: **18 ativos e 4 inativos**. Os quatro inativos evitam caminhos ambíguos:

- `profissionais[codigo_filial]` → `filiais[codigo_filial]`
- `vendedores[codigo_filial]` → `filiais[codigo_filial]`
- `metas_valor[codigo_grupo_servico]` → `grupos_servico[codigo_grupo_servico]`
- `metas_quantidade[codigo_grupo_servico]` → `grupos_servico[codigo_grupo_servico]`

**Atenção:** a relação entre `servicos` e `grupos_servico` permanece ativa. Metas de nível Produto precisam de tratamento específico no DAX por causa do caminho de filtros; não ativar indiscriminadamente as relações inativas.

O calendário foi marcado como tabela de datas; ordenar `mes_ano` por `ano_mes` e `mes_nome` por `mes_numero`.

Para as chaves das 11 tabelas e o inventário das 22 ligações, consultar [análise do dicionário](f01-02-analise-dicionario-dados.md). Para as razões e testes das relações ativas/inativas, ver [configuração do modelo](f01-05-relacionamentos-modelo.md) e [validação do calendário/modelo](f01-06-07-validacao-calendario-modelo.md).
