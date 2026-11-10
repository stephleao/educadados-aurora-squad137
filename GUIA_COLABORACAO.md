# Guia de colaboração — Painel Aurora | Squad 137

Regras de trabalho reutilizáveis nas fases do bootcamp.

## Arquivos no Drive e no GitHub

- **Google Drive:** planilhas, recursos visuais e arquivos `.pbix` de trabalho e de entrega.
- **GitHub:** Issues, documentação Markdown, medidas `.dax` e Pull Requests. Não enviar `.pbix` para o repositório.
- Cada fase usa as pastas `01 WIP` (desenvolvimento) e `02 Entrega` (versão final).
- Nome no WIP: `Aurora_[TAREFA]_[RESPONSÁVEL].pbix`, com `_wip` ou `_incompleto` quando necessário.
- Nome final: `Aurora_squad_137_fXX_final.pbix` (substituir `XX` pelo número da fase).
- Manter a versão de trabalho mais recente; antes de apagar versões antigas, confirmar que nenhuma contribuição será perdida.

## Desenvolvimento e integração

- Quem desenvolve uma tarefa **testa e integra a própria contribuição**.
- Apenas uma pessoa deve editar o `.pbix` principal por vez; combinar o horário, conferir a versão atual e avisar a equipe após salvar.
- A conferência final verifica coletivamente se as contribuições foram incorporadas e se o relatório funciona.

## GitHub e revisão

- Para documentação e `.dax`, trabalhar em branch própria, apresentar alterações para revisão e abrir Pull Request antes de integrar à `main`.
- Usar `Assignees` para quem desenvolve e **`Revisor` na descrição da Issue** para a pessoa que confere.
- Preferencialmente, o revisor será quem executará a próxima tarefa dependente. Quando não for possível, escolher outro integrante; **ninguém aprova a própria tarefa**.
- O revisor verifica todos os itens do checklist e o critério de conclusão, diretamente no `.pbix`, no DAX, nos documentos ou no Drive. Se houver problemas, devolve para correção e depois revisa novamente.
- Mover a tarefa para `Concluído` significa que a revisão foi aprovada; **não é necessário comentário de aprovação** nem print rotineiro.
- Atividades expressamente marcadas como **revisão coletiva** no planejamento ou na Issue envolvem toda a squad, sem substituir a revisão individual das outras tarefas.
- Usar a label `Impedida` somente quando houver bloqueio real, removendo-a após resolver o impedimento.

## Entrega oficial

- Conferir o prazo e os requisitos da fase.
- Guardar o `.pbix` final no Google Drive e publicar o painel pelo método exigido no bootcamp.
- Testar os dois links em janela anônima, sem login, e guardar prints de publicação quando exigidos.
