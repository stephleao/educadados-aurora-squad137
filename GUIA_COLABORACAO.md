# Guia de colaboração — Painel Aurora | Squad 137

Este guia reúne regras de colaboração reutilizáveis nas fases do bootcamp.

## Onde guardar os arquivos

- **Google Drive:** planilhas, logomarca e arquivos `.pbix` de trabalho e entrega.
- **GitHub:** Issues, documentação Markdown e fórmulas `.dax`.
- Não enviar arquivos `.pbix` ao repositório.

## Estrutura do Google Drive por fase

```text
Fase X/
├── 01 WIP/
└── 02 Entrega/
```

## Nomes dos arquivos e versões

- Em `01 WIP`: `Aurora_[TAREFA]_[RESPONSÁVEL].pbix`, por exemplo `Aurora_f02_01_steph.pbix`.
- Acrescentar `_wip` ou `_incompleto` antes de `.pbix` quando ainda não estiver finalizado.
- Manter somente a versão mais recente ou uma versão incompleta relevante. Antes de excluir uma cópia, confirmar que nenhuma contribuição útil será perdida.
- Em `02 Entrega`: `Aurora_squad_137_fXX_final.pbix` (substituir `XX` pelo número da fase), junto aos registros de publicação, quando exigidos.

## Responsabilidade de integração

- Quem desenvolve a tarefa também testa e integra sua contribuição no `.pbix` de trabalho.
- Apenas uma pessoa edita o `.pbix` principal por vez. Combinar horários de edição com a equipe.
- Antes de editar, confirmar a versão atual; depois de salvar, comunicar onde está a versão atualizada e o que mudou.
- Integração final significa conferir coletivamente se todas as contribuições foram incorporadas e se o relatório continua funcionando; não transferir toda a integração para uma única pessoa.

## GitHub e revisão

- Criar branches próprias para alterações em documentação e `.dax`.
- Apresentar as alterações propostas para revisão antes de commitar.
- Abrir Pull Request e revisar antes do merge em `main`.
- Usar Issues para registrar checklists, dependências e critérios de conclusão.
- **Revisão das tarefas:** o revisor deve percorrer todos os itens do checklist e verificar se o critério de conclusão foi atendido. A conferência pode ser feita diretamente no `.pbix`, no DAX, na documentação ou no Drive, conforme a tarefa. Prints só são necessários quando agregarem valor; os registros de publicação ficam na entrega.

## Entrega oficial

- Confirmar requisitos e prazo próprios de cada fase.
- Publicar o painel pelo método exigido pelo bootcamp e disponibilizar o `.pbix` no Google Drive.
- Testar ambos os links em janela anônima, sem login; guardar prints de publicação quando aplicável.
