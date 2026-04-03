# Change Log

All notable changes to the "monokai-black-wal" extension will be documented in this file.

## [1.7.0] - 2026-04-03

### Added
- Bracket Pair Colorization — 6 níveis de cores para `{}[]()` aninhados (`editorBracketHighlight.foreground1-6`)
- Bracket Matching — destaque roxo ao clicar em bracket (`editorBracketMatch`)
- Diff Editor — fundos suaves verde/vermelho alinhados à paleta (`diffEditor.*`)
- Code Folding — ícone verde e fundo sutil na linha dobrada (`editor.foldBackground`, `editorGutter.foldingControlForeground`)
- Status Bar states — cores por estado: erro rosa, warning amarelo, debugging (`statusBarItem.*`, `statusBar.debugging*`)
- Overview Ruler — marcadores de erro/warning/git usando paleta do tema (`editorOverviewRuler.*`)
- Search highlights — range de busca com fundo suave (`editor.findRangeHighlightBackground`, `editor.rangeHighlightBackground`)
- Tabs modified border — borda verde na aba ativa com alterações (`tab.activeModifiedBorder`, `tab.inactiveModifiedBorder`)
- Keybinding labels — fundo e borda alinhados ao tema (`keybindingLabel.*`)
- Symbol Icons — 22 tokens por tipo de símbolo (class, method, variable, enum, etc.) (`symbolIcon.*`)
- Cursor verde da paleta (`editorCursor.foreground: #a6e22e`)
- Testing icons — pass verde, fail rosa, pending cinza (`testing.*`)
- Lightbulb e problem icons alinhados à paleta (`editorLightBulb.*`, `problemsErrorIcon.*`)
- Copilot/Chat — painel integrado ao tema (`chat.*`, `chatVariable.*`)
- Notebook/Jupyter — células com bordas da paleta (`notebook.*`, `notebookStatus*`)
- Checkbox verde e tree indent guides (`checkbox.*`, `tree.*`)
- Welcome Page integrada ao tema preto (`welcomePage.*`, `textBlockQuote.*`, `textCodeBlock.*`)
- `editorUnnecessaryCode.opacity` — variáveis não utilizadas com opacidade reduzida
- Semantic modifiers desconstruídos de `*` para tipos específicos: `function/method/class.declaration`, `method/property.static`, `class/method.abstract`, `function/method.async`, `comment.documentation`, `function/class/variable.defaultLibrary`
- Scopes por linguagem: Rust lifetimes (`#ae81ff`), SCSS variables (`#FD971F`), JSX/TSX props, Python decorators/type hints/built-ins, Go structs/interfaces/funções, template literals JS/TS (`${}`), regex groups/assertions, Shell/Bash funções e variáveis

### Fixed
- `entity.name.function.dart` duplicado em duas regras com cores conflitantes — removido de "Keyword, Storage", mantido só em "Function dart" (`#2EA6E2 bold`)
- `constant.other.color` duplicado em "Operator, Misc" — removido
- `markup.raw.block.fenced.markdown` em duas regras (`#546E7A` vs `#EEFFFF`) — unificado em `#EEFFFF`
- `variable.language.fenced.markdown` em duas regras — unificado em `#65737E`
- `property` semântico (`#eeffff`) conflitando com `entity.other.attribute-name` — alinhado
- `*.readonly` sobrescrevendo cores indevidamente — desconstruído em `property.readonly`, `property.readonly.declaration` e `variable.readonly`
- JSON strings com cor `#cfcfc2` (confundia com comentários) — corrigido para `#e6db74`
- `*.readonly` cor fora da paleta (`#2a8ee0`) corrigida para `#66d9ef`

### Changed
- `property` (semantic token) — cor ajustada para `#64B5F6` (azul céu claro)
- `property.readonly` — `#42A5F5` itálico (uso) e `#eeffff` itálico (declaração)
- `variable.language` (`this`, `self`) — cor ajustada para `#ae81ff` itálico
- `interface` (semantic token) — diferenciado de `storage.type` com `#a6e22e`

## [1.6.1] - 2026-04-01

### Added
- `LICENSE` file (MIT)
- Ko-fi sponsor link no README e no `package.json`
- Badges de Version, Installs, Downloads e License no README

### Changed
- Ícone atualizado para `assets/banner.png`
- Keywords expandidas com `walteann`, `dart`, `flutter`, `semantic`, `pure black`

## [1.6.0] - 2026-04-01

### Added
- `button.*` — botões nativos (diálogos, notificações) com cor verde do tema no primário
- `editorGutter.addedBackground`, `modifiedBackground`, `deletedBackground` — indicadores de diff Git no gutter
- `editorError.*`, `editorWarning.*`, `editorInfo.*` — squiggles de erro (rosa), warning (amarelo) e info (ciano)
- `editorInlayHint.*` — inlay hints com fundo azul escuro e texto diferenciado por tipo e parâmetro
- `merge.*` — regiões de merge conflict coloridas: verde (current) vs ciano (incoming)
- `galleryBanner` — banner preto no Marketplace para consistência com o tema dark
- `author` e `bugs.url` no `package.json` para visibilidade no Marketplace
- Banner de hero (`assets/banner-readme.png`) no topo do README

### Fixed
- `support.type` duplicado em duas regras com cores conflitantes — unificado em ciano (`#66d9ef`)
- `keyword.control.from` presente em dois blocos — removido da regra genérica, mantido apenas na regra com `fontStyle: italic`
- Marcadores de fenced code block no Markdown (`markup.raw.block.fenced.markdown`, `punctuation.definition.fenced.markdown`) estavam com cor `#00000050` (invisível no fundo preto) — corrigido para `#546E7A`
- Scopes comentados mortos removidos (`// "keyword"` e `// "keyword.control"`)

### Changed
- `description` no `package.json` atualizado para texto descritivo e buscável no Marketplace
- `license: "MIT"` adicionado ao `package.json`
- Screenshots atualizadas com capturas reais do tema ativo (`preview-tsx`, `preview-css`, `preview-ts`, `preview-html`, `preview-dart`)

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
