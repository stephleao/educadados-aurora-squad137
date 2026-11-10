# Regras de negócio — Fase 1

Referência: enunciado do Desafio Fase 1 e descrição da base Educadados. **Não confundir número de vendas com quantidade de itens, nem valor líquido das vendas com valor bruto dos itens.**

| Corte | Valor realizado | Quantidade realizada | Regra da meta |
|---|---|---|---|
| Rede | `vendas[valor_liquido]` | Número de vendas | Soma das metas das filiais |
| Filial | Valor líquido | Número de vendas | Valor: nível **Produto**; quantidade: nível **Vendedor** |
| Cidade | Valor líquido das filiais da cidade | Número de vendas | Soma das metas de suas filiais |
| Vendedor | Valor líquido | Número de vendas | Nível **Vendedor** |
| Profissional | Valor líquido | Número de vendas | Nível **Profissional** |
| Grupo de serviço | `itens_venda[valor_total]` (bruto) | Soma de `itens_venda[quantidade]` | Nível **Produto** |
| Serviço | Valor bruto dos itens | Quantidade de itens | Nível **Serviço** |

## Cuidados de cálculo

- O valor líquido considera o desconto da venda; o valor bruto de itens **não** contém desconto rateado.
- As metas têm quatro níveis independentes (Produto, Serviço, Vendedor e Profissional). **Nunca somar níveis diferentes**, pois isso duplica o objetivo.
- Meta inexistente deve aparecer como **"sem meta"**, não como 0%; manter medidas numéricas separadas de textos de exibição.
- As vendas vão de **01/01/2024 a 30/09/2026**. Metas cadastradas até dezembro/2026 não implicam vendas futuras.

## Perguntas de aprovação — setembro/2026

1. Qual o valor líquido da rede e o percentual da meta de valor (uma casa decimal)?
2. Qual filial lidera em valor líquido e qual seu percentual de atingimento?
3. Qual cidade lidera em **número de vendas**? Ela também lidera em valor líquido?
4. Entre vendedores com meta de valor, quem tem o menor percentual de atingimento?
5. Qual grupo de serviço lidera em **valor bruto dos itens** e qual sua participação no total bruto?

As respostas dependem das planilhas reais; não registrar valores não validados.
