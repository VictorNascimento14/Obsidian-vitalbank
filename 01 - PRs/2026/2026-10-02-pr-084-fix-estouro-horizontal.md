---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 84
url: https://github.com/VictorNascimento14/Vitalbank/pull/84
branch: fix/estouro-horizontal-no-celular
tags: [pr, bug, layout, responsivo]
status: aberto
---

# PR #84 — fix(layout): impedir que a fila de cartões alargue a página no celular

## 🎯 Contexto

Bug de layout do celular, achado ao capturar Transações. Afeta [[2026-10-02-pr-052-visao-geral-meus-cartoes]] em diante. Fecha a issue #83.

## 🔧 Mudanças

- `src/app/(painel)/page.tsx`, `src/app/(painel)/transacoes/page.tsx` — `grid-cols-1`.

## ⚠️ Armadilhas e aprendizados

- Coluna implícita de grade é `auto`, e `auto` respeita o **conteúdo mínimo** do item — inclusive o de um filho com rolagem interna. `grid-cols-1` do Tailwind é `minmax(0, 1fr)`, que deixa o item encolher. Ver [[2026-10-02-grade-sem-minmax-alarga-com-rolagem-interna]].

## 🧪 Como testar

1. Playwright em 375 px: `scrollWidth` = 375 em `/`, `/transacoes` e `/contas`.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[Transacoes]]
- [[2026-10-02-grade-sem-minmax-alarga-com-rolagem-interna]]
- [[2026]] (changelog)
