---
tipo: componente
camada: ui
arquivo: src/ui/casca/Casca.tsx
ultima_atualizacao: 2026-10-02
tags: [casca, layout]
---

# Casca

Montada **uma vez** por `src/app/(painel)/layout.tsx`; só o `<main id="conteudo">` troca ao navegar.

- **≥ `lg` (1024 px):** [[ColunaLateral]] fixa (`sticky`, altura da tela) + [[Cabecalho]] + miolo.
- **< `lg`:** a coluna mora numa **gaveta** (`role="dialog"`, `aria-modal`): véu com fade, painel em mola; fecha com Esc, clique no véu ou ao navegar; trava a rolagem; foco entra no primeiro link e volta ao ☰.
- "Pular para o conteúdo" no topo, visível ao focar.

A cada navegação o miolo entra (opacidade + 12 px): um `motion.div` com `key` na rota, dentro da casca — [[2026-10-02-pr-158-transicao-entre-telas]], movido do `template.tsx` em [[2026-10-02-pr-192-fix-transicao-sem-template]].

Tela que ainda não chegou usa `EmBreve`.

Introduzido em [[2026-10-02-pr-046-layout-do-painel]].
