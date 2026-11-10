# F01-05 — Relacionamentos do modelo

Foram configurados os **22 relacionamentos** previstos no dicionário, todos `*:1` com filtro em direção única: **18 ativos e 4 inativos**.

| Relacionamento inativo | Motivo |
|---|---|
| `profissionais[codigo_filial]` → `filiais[codigo_filial]` | Evitar caminho duplo entre filial, vendas e metas. |
| `vendedores[codigo_filial]` → `filiais[codigo_filial]` | Evitar caminho duplo entre filial, vendas e metas. |
| `metas_valor[codigo_grupo_servico]` → `grupos_servico[codigo_grupo_servico]` | Evitar caminho ambíguo pelo serviço. |
| `metas_quantidade[codigo_grupo_servico]` → `grupos_servico[codigo_grupo_servico]` | Evitar caminho ambíguo pelo serviço. |

A relação `servicos[codigo_grupo_servico]` → `grupos_servico[codigo_grupo_servico]` segue ativa e permite filtrar itens por grupo. Nos testes iniciais, **filial, profissional, vendedor, serviço, grupo e calendário** responderam aos filtros esperados; nulos legítimos das metas foram confirmados.

**Ponto de atenção:** as metas do nível Produto exigem tratamento específico de filtro no DAX, pois o relacionamento direto com grupos está inativo. Metas sem cadastro devem ser exibidas como "sem meta". Os níveis Produto, Serviço, Vendedor e Profissional não devem ser somados entre si.

Estes são os testes iniciais do modelo, **não a aprovação de todos os valores finais**. Ver também [validações F01-06 e F01-07](f01-06-07-validacao-calendario-modelo.md).
