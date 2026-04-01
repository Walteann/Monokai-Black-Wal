# Change Log

All notable changes to the "monokai-black-wal" extension will be documented in this file.

## [1.5.0] - 2026-04-01

### Added
- Semantic highlighting (`semanticHighlighting: true` + `semanticTokenColors`) com suporte a class, type, interface, enum, function, method, parameter, variable, decorator e modificadores (`*.readonly`, `*.static`, `*.declaration`, `*.deprecated`, `*.abstract`)
- Terminal integrado: paleta ANSI completa de 16 cores fiel à paleta do tema, cursor verde e seleção
- `editorStickyScroll.*` — sticky scroll background e hover
- `breadcrumb.*` — barra de navegação de contexto
- `gitDecoration.*` — colorização de arquivos no Explorer por status git (added, modified, deleted, untracked, ignored, conflicting)
- `minimap.*` e `minimapGutter.*` — minimap e indicadores de diff no gutter
- `list.*` — hover, foco e seleção de listas e tree views
- `input.*` — campos de input, placeholder e validação (erro/warning)
- `panel.*` — painel inferior (terminal, problemas, output)
- `badge.*` — badges e contadores numéricos com cor verde do tema
- `editorGroup.*` e `tab.*` adicionais — borda superior verde na aba ativa, foreground ativo/inativo
- `scrollbar.*` — trilho e alça do scrollbar
- `peekView.*` — peek view (go-to-definition inline)
- `notifications.*`, `dropdown.*`, `quickInput.*` — widgets da UI
- `editor.selectionBackground`, `editor.wordHighlightBackground`, `editor.findMatch*` — destaques do editor
- `editorSuggestWidget.*` — widget de autocomplete
- `editorIndentGuide.background1` — guias de indentação normais em cinza

### Fixed
- `editorIndentGuide.activeBackground` substituído por `editorIndentGuide.activeBackground1` (token deprecado desde VSCode 1.71)
- `activityBarBadge.background` alinhado à paleta verde (`#a6e22e`)

### Changed
- `engines.vscode` atualizado de `^1.67.0` para `^1.75.0`

## [1.4.0]

- Melhoria no focus da linha em digitação

## [1.3.7]

- Update colors to dart

## [1.3.6]

- Melhorias gerais de cores
