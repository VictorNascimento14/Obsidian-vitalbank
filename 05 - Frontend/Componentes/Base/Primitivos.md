---
tipo: componente
camada: ui
arquivo: src/ui/base/
ultima_atualizacao: 2026-10-02
tags: [design, primitivos]
---

# Primitivos

Peças de `src/ui/base/`, importadas de `@/ui`. Tokens em [[linguagem-visual]].

| Peça | O que é | PR |
|---|---|---|
| `Bloco` | superfície branca, canto 25 px; `colado` sem respiro | [[2026-10-02-pr-024-bloco-e-titulo]] |
| `TituloDeSecao` | `h2` 18/22 px com `acao` à direita | [[2026-10-02-pr-024-bloco-e-titulo]] |
| `Botao` | sólido, contorno, fantasma; `md`/`sm`; campo ou pílula; sobe no hover e afunda no toque; `type="button"` padrão | [[2026-10-02-pr-026-botao]] |
| `Campo` | input com rótulo, `dica` e `erro` (`aria-describedby`, `aria-invalid`); halo de foco | [[2026-10-02-pr-028-campo]] |
| `Avatar` | iniciais sobre gradiente de tokens escolhido por hash do nome; sem foto (ADR-002) | [[2026-10-02-pr-030-avatar]] |
| `Alternador` | `role="switch"`, controlado ou não; bolinha desliza em mola, trilho turquesa | [[2026-10-02-pr-032-alternador]] |
| `Abas` | WAI-ARIA com setas/Home/End; sublinhado desliza (`layoutId`), painel em fade | [[2026-10-02-pr-034-abas]] |
| `PastilhaDeIcone` | círculo claro + ícone Remix colorido; 6 tons; gira e cresce com `group-hover` | [[2026-10-02-pr-036-pastilha-de-icone]] |
| `Paginacao` | "Anterior 1 2 3 Próxima"; página atual em pílula que desliza; controlada | [[2026-10-02-pr-088-paginacao]] |
