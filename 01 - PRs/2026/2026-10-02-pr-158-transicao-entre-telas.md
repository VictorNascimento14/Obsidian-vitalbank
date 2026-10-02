---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 158
url: https://github.com/VictorNascimento14/Vitalbank/pull/158
branch: ui/transicao-entre-telas
tags: [pr, casca, animacao]
status: aberto
---

# PR #158 — ui(casca): transição suave do conteúdo a cada troca de tela

## 🎯 Contexto

Sistema, item 1. Fecha a issue #157.

## 🔧 Mudanças

- `src/app/(painel)/template.tsx` + teste.

## 🧠 Decisões técnicas

- **`template.tsx`, não `layout.tsx`**: o Next remonta o template a cada navegação (ele recebe uma `key` por segmento), e mantém o layout. A animação de entrada acontece de novo sem remontar a casca — que precisa ficar parada para o marcador do menu deslizar ([[ColunaLateral]]).
- **Sem animação de saída**: esperar a tela velha sair atrasaria a nova; entrada curta basta.
- Lido em `node_modules/next/dist/docs/…/template.md` (Next 16), como manda o `AGENTS.md`.

## 🧪 Como testar

1. `pnpm build` e navegação no `pnpm dev`.

## 📎 Documentação afetada

- [[Casca]]
- [[2026]] (changelog)
